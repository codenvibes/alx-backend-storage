<h1 align="center"><b>0X02. REDIS BASIC</b></h1>
<div align="center"><code>Back-end</code> <code>Redis</code></div>

<br><div align="center"><img width="70%" src="https://github.com/codenvibes/alx-backend-storage/blob/master/0x02-redis_basic/images/40eab4627f1bea7dfe5e.png"></div>

<!-- <br>
<hr>
<h3><a href=>Notes</a></h3>
<hr> -->


<!--==================================================-->
<br>

## Resources
<details>
<summary><b><a href="https://www.youtube.com/watch?v=Hbt56gFj998">Redis Crash Course Tutorial</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://redis.io/docs/latest/commands/">Redis commands</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://redis-py.readthedocs.io/en/stable/">Redis python client</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://realpython.com/python-redis/">How to Use Redis With Python</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>



<!--==================================================-->
<br>

## Learning Objectives
<details>
<summary><b><a href=" "> </a>Learn how to use redis for basic operations</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>Learn how to use redis as a simple cache</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>



<br>

<!--==================================================-->
<br>

## Requirements
- All of your files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
- All of your files should end with a new line
- A <code>README.md</code> file, at the root of the folder of the project, is mandatory
- The first line of all your files should be exactly <code>#!/usr/bin/env python3</code>
- Your code should use the <code>pycodestyle</code> style (version 2.5)
- All your modules should have documentation (<code>python3 -c 'print(__import__("my_module").__doc__)'</code>)
- All your classes should have documentation (<code>python3 -c 'print(__import__("my_module").MyClass.__doc__)'</code>)
- All your functions and methods should have documentation (<code>python3 -c 'print(__import__("my_module").my_function.__doc__)'</code> and <code>python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'</code>)
- A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
- All your functions and coroutines must be type-annotated.

<!--==================================================-->
<br>

## Install Redis on Ubuntu 18.04
<pre><code>$ sudo apt-get -y install redis-server
$ pip3 install redis
$ sed -i "s/bind .*/bind 127.0.0.1/g" /etc/redis/redis.conf
</code></pre>


<!--==================================================-->
<br>

## Use Redis in a container
Redis server is stopped by default - when you are starting a container, you should start it with: <code>service redis-server start</code>


<!--==================================================-->
<br>

## Tasks
<details>
<summary>

### 0. Writing strings to Redis
`mandatory`

File: [exercise.py]()
</summary>

<p>Create a <code>Cache</code> class. In the <code>__init__</code> method, store an instance of the Redis client as a private variable named <code>_redis</code> (using <code>redis.Redis()</code>) and flush the instance using <code>flushdb</code>.</p>

<p>Create a <code>store</code> method that takes a <code>data</code> argument and returns a string. The method should generate a random key (e.g. using <code>uuid</code>), store the input data in Redis using the random key and return the key.</p>

<p>Type-annotate <code>store</code> correctly. Remember that <code>data</code> can be a <code>str</code>, <code>bytes</code>, <code>int</code> or <code>float</code>.</p>

<pre><code>bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
import redis

Cache = __import__('exercise').Cache

cache = Cache()

data = b"hello"
key = cache.store(data)
print(key)

local_redis = redis.Redis()
print(local_redis.get(key))

bob@dylan:~$ python3 main.py 
3a3e8231-b2f6-450d-8b0e-0f38f16e8ca2
b'hello'
bob@dylan:~$ 
</code></pre>


</details>

<details>
<summary>

### 1. Reading from Redis and recovering original type
`mandatory`

File: [exercise.py]()
</summary>

<p>Redis only allows to store string, bytes and numbers (and lists thereof). Whatever you store as single elements, it will be returned as a byte string. Hence if you store <code>"a"</code> as a UTF-8 string, it will be returned as <code>b"a"</code> when retrieved from the server.</p>

<p>In this exercise we will create a <code>get</code> method that take a <code>key</code> string argument and an optional <code>Callable</code> argument named <code>fn</code>. This callable will be used to convert the data back to the desired format.</p>

<p>Remember to conserve the original <code>Redis.get</code> behavior if the key does not exist.</p>

<p>Also, implement 2 new methods: <code>get_str</code> and <code>get_int</code> that will automatically parametrize <code>Cache.get</code> with the correct conversion function.</p>

<p>The following code should not raise:</p>

<pre><code class="python">cache = Cache()

TEST_CASES = {
    b"foo": None,
    123: int,
    "bar": lambda d: d.decode("utf-8")
}

for value, fn in TEST_CASES.items():
    key = cache.store(value)
    assert cache.get(key, fn=fn) == value
</code></pre>


</details>

<details>
<summary>

### 2. Incrementing values
`mandatory`

File: [exercise.py]()
</summary>

<p>Familiarize yourself with the <code>INCR</code> command and its python equivalent.</p>

<p>In this task, we will implement a system to count how many times methods of the <code>Cache</code> class are called.</p>

<p>Above <code>Cache</code> define a <code>count_calls</code> decorator that takes a single <code>method</code> <code>Callable</code> argument and returns a <code>Callable</code>.</p>

<p>As a key, use the qualified name of <code>method</code> using the <code>__qualname__</code> dunder method.</p>

<p>Create and return function that increments the count for that key every time the method is called and returns the value returned by the original method.</p>

<p>Remember that the first argument of the wrapped function will be <code>self</code> which is the instance itself, which lets you access the Redis instance.</p>

<p>Protip: when defining a decorator it is useful to use <code>functool.wraps</code> to conserve the original function’s name, docstring, etc. Make sure you use it as described <a href="https://intranet.alxswe.com/rltoken/eRjLY2hVLrkDcNkcDJDK3g" target="_blank" title="here">here</a>.</p>

<p>Decorate <code>Cache.store</code> with <code>count_calls</code>.</p>

<pre><code>bob@dylan:~$ cat main.py
#!/usr/bin/env python3
""" Main file """

Cache = __import__('exercise').Cache

cache = Cache()

cache.store(b"first")
print(cache.get(cache.store.__qualname__))

cache.store(b"second")
cache.store(b"third")
print(cache.get(cache.store.__qualname__))

bob@dylan:~$ ./main.py
b'1'
b'3'
bob@dylan:~$ 
</code></pre>


</details>

<details>
<summary>

### 3. Storing lists
`mandatory`

File: [exercise.py]()
</summary>

<p>Familiarize yourself with redis commands <code>RPUSH</code>, <code>LPUSH</code>, <code>LRANGE</code>, etc.</p>

<p>In this task, we will define a <code>call_history</code> decorator to store the history of inputs and outputs for a particular function.</p>

<p>Everytime the original function will be called, we will add its input parameters to one list in redis, and store its output into another list.</p>

<p>In <code>call_history</code>, use the decorated function’s qualified name and append <code>":inputs"</code> and <code>":outputs"</code> to create input and output list keys, respectively.</p>

<p><code>call_history</code> has a single parameter named <code>method</code> that is a <code>Callable</code> and returns a <code>Callable</code>.</p>

<p>In the new function that the decorator will return, use <code>rpush</code> to append the input arguments. Remember that Redis can only store strings, bytes and numbers. Therefore, we can simply use <code>str(args)</code> to normalize. We can ignore potential <code>kwargs</code> for now.</p>

<p>Execute the wrapped function to retrieve the output. Store the output using <code>rpush</code> in the <code>"...:outputs"</code> list, then return the output.</p>

<p>Decorate <code>Cache.store</code> with <code>call_history</code>.</p>

<pre><code>bob@dylan:~$ cat main.py
#!/usr/bin/env python3
""" Main file """

Cache = __import__('exercise').Cache

cache = Cache()

s1 = cache.store("first")
print(s1)
s2 = cache.store("secont")
print(s2)
s3 = cache.store("third")
print(s3)

inputs = cache._redis.lrange("{}:inputs".format(cache.store.__qualname__), 0, -1)
outputs = cache._redis.lrange("{}:outputs".format(cache.store.__qualname__), 0, -1)

print("inputs: {}".format(inputs))
print("outputs: {}".format(outputs))

bob@dylan:~$ ./main.py
04f8dcaa-d354-4221-87f3-4923393a25ad
a160a8a8-06dc-4934-8e95-df0cb839644b
15a8fd87-1f55-4059-86aa-9d1a0d4f2aea
inputs: [b"('first',)", b"('secont',)", b"('third',)"]
outputs: [b'04f8dcaa-d354-4221-87f3-4923393a25ad', b'a160a8a8-06dc-4934-8e95-df0cb839644b', b'15a8fd87-1f55-4059-86aa-9d1a0d4f2aea']
bob@dylan:~$ 
</code></pre>


</details>

<details>
<summary>

### 4. Retrieving lists
`mandatory`

File: [exercise.py]()
</summary>

<p>In this tasks, we will implement a <code>replay</code> function to display the history of calls of a particular function.</p>

<p>Use keys generated in previous tasks to generate the following output:</p>

<pre><code>&gt;&gt;&gt; cache = Cache()
&gt;&gt;&gt; cache.store("foo")
&gt;&gt;&gt; cache.store("bar")
&gt;&gt;&gt; cache.store(42)
&gt;&gt;&gt; replay(cache.store)
Cache.store was called 3 times:
Cache.store(*('foo',)) -&gt; 13bf32a9-a249-4664-95fc-b1062db2038f
Cache.store(*('bar',)) -&gt; dcddd00c-4219-4dd7-8877-66afbe8e7df8
Cache.store(*(42,)) -&gt; 5e752f2b-ecd8-4925-a3ce-e2efdee08d20
</code></pre>

<p>Tip: use <code>lrange</code> and <code>zip</code> to loop over inputs and outputs.</p>


</details>

<details>
<summary>

### 5. Implementing an expiring web cache and tracker
`#advanced`

File: [web.py]()
</summary>

<p>In this tasks, we will implement a <code>get_page</code> function (prototype: <code>def get_page(url: str) -&gt; str:</code>). The core of the function is very simple. It uses the <code>requests</code> module to obtain the HTML content of a particular URL and returns it.</p>

<p>Start in a new file named <code>web.py</code> and do not reuse the code written in <code>exercise.py</code>.</p>

<p>Inside <code>get_page</code> track how many times a particular URL was accessed in the key <code>"count:{url}"</code> and cache the result with an expiration time of 10 seconds.</p>

<p>Tip: Use <code>http://slowwly.robertomurray.co.uk</code> to simulate a slow response and test your caching.</p>

<p>Bonus: implement this use case with decorators.</p>


</details>

