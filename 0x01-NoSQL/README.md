<h1 align="center"><b>0X01. NOSQL</b></h1>
<div align="center"><code>Back-end</code> <code>NoSQL</code> <code>MongoDB</code></div>

<!-- <br>
<hr>
<h3><a href=>Notes</a></h3>
<hr> -->


<!--==================================================-->
<br>

## Resources
<details>
<summary><b><a href="https://riak.com/resources/nosql-databases/">NoSQL Databases Explained</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://www.youtube.com/watch?v=qUV2j3XBRHc">What is NoSQL ?</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://intranet.alxswe.com/rltoken/RyyP9OH1EMBWWYpTs4TqoA">MongoDB with Python Crash Course - Tutorial for Beginners</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://intranet.alxswe.com/rltoken/9__3tR-NimgXlmjPQwTF-Q">MongoDB Tutorial 2 : Insert, Update, Remove, Query</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://intranet.alxswe.com/rltoken/ziEDeniRobC6owPE1_avAQ">Aggregation</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://intranet.alxswe.com/rltoken/axwwF4CjO7FnK8Ecochqnw">Introduction to MongoDB and Python</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://intranet.alxswe.com/rltoken/lUqnLwOHbbp9FK39ijNmDQ">mongo Shell Methods</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href="https://intranet.alxswe.com/rltoken/ipHIVVmAsezINqpk7W0eow">Mongosh</a></b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>



<!--==================================================-->
<br>

## Learning Objectives
<h3>General</h3>

<details>
<summary><b><a href=" "> </a>What NoSQL means</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>What is difference between SQL and NoSQL</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>What is ACID</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>What is a document storage</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>What are NoSQL types</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>What are benefits of a NoSQL database</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>How to query information from a NoSQL database</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>How to insert/update/delete information from a NoSQL database</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>


<details>
<summary><b><a href=" "> </a>How to use MongoDB</b></summary><br>


<br><p align="center">※※※※※※※※※※※※</p><br>
</details>



<br>

<!--==================================================-->
<br>

## Requirements
<h3>MongoDB Command File</h3>

- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using <code>MongoDB</code> (version 4.2)
- All your files should end with a new line
- The first line of all your files should be a comment: <code>// my comment</code>
- A <code>README.md</code> file, at the root of the folder of the project, is mandatory
- The length of your files will be tested using <code>wc</code>
<h3>Python Scripts</h3>

- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using <code>python3</code> (version 3.7) and <code>PyMongo</code> (version 3.10)
- All your files should end with a new line
- The first line of all your files should be exactly <code>#!/usr/bin/env python3</code>
- A <code>README.md</code> file, at the root of the folder of the project, is mandatory
- Your code should use the <code>pycodestyle</code> style (version 2.5.*)
- The length of your files will be tested using <code>wc</code>
- All your modules should have a documentation (<code>python3 -c 'print(__import__("my_module").__doc__)'</code>)
- All your functions should have a documentation (<code>python3 -c 'print(__import__("my_module").my_function.__doc__)'</code>
- Your code should not be executed when imported (by using <code>if __name__ == "__main__"</code>:)

<!--==================================================-->
<br>

## More Info
<h3>Install MongoDB 4.2 in Ubuntu 18.04</h3>

<a href="https://intranet.alxswe.com/rltoken/8p4x14Ddn1UxKXZ5nPt3zA" target="_blank" title="Official installation guide">Official installation guide</a>

<pre><code>$ wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | apt-key add -
$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" &gt; /etc/apt/sources.list.d/mongodb-org-4.2.list
$ sudo apt-get update
$ sudo apt-get install -y mongodb-org
...
$  sudo service mongod status
mongod start/running, process 3627
$ mongo --version
MongoDB shell version v4.2.8
git version: 43d25964249164d76d5e04dd6cf38f6111e21f5f
OpenSSL version: OpenSSL 1.1.1  11 Sep 2018
allocator: tcmalloc
modules: none
build environment:
    distmod: ubuntu1804
    distarch: x86_64
    target_arch: x86_64
$  
$ pip3 install pymongo
$ python3
&gt;&gt;&gt; import pymongo
&gt;&gt;&gt; pymongo.__version__
'3.10.1'
</code></pre>

Potential issue if documents creation doesn’t work or this error: <code>Data directory /data/db not found., terminating</code> (<a href="https://intranet.alxswe.com/rltoken/as8vd5VBnj4VDz5EINszMg" target="_blank" title="source">source</a> and <a href="https://intranet.alxswe.com/rltoken/9Df5v1NcWFFCn_sRNgsJUg" target="_blank" title="source">source</a>)

<pre><code>$ sudo mkdir -p /data/db
</code></pre>

Or if <code>/etc/init.d/mongod</code> is missing, please find here an example of the file:

<details>
<summary>Click to expand/hide file contents</summary>
<pre><code>
#!/bin/sh
### BEGIN INIT INFO
# Provides:          mongod
# Required-Start:    $network $local_fs $remote_fs
# Required-Stop:     $network $local_fs $remote_fs
# Should-Start:      $named
# Should-Stop:
# Default-Start:     2 3 4 5
# Default-Stop:      0 1 6
# Short-Description: An object/document-oriented database
# Description:       MongoDB is a high-performance, open source, schema-free
#                    document-oriented data store that's easy to deploy, manage
#                    and use. It's network accessible, written in C++ and offers
#                    the following features:
#
#                       * Collection oriented storage - easy storage of object-
#                         style data
#                       * Full index support, including on inner objects
#                       * Query profiling
#                       * Replication and fail-over support
#                       * Efficient storage of binary data including large
#                         objects (e.g. videos)
#                       * Automatic partitioning for cloud-level scalability
#
#                    High performance, scalability, and reasonable depth of
#                    functionality are the goals for the project.
### END INIT INFO

PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin
DAEMON=/usr/bin/mongod
DESC=database

NAME=mongod
# Defaults.  Can be overridden by the /etc/default/$NAME
# Other configuration options are located in $CONF file. See here for more:
# http://dochub.mongodb.org/core/configurationoptions
CONF=/etc/mongod.conf
PIDFILE=/var/run/$NAME.pid
ENABLE_MONGOD=yes

# Include mongodb defaults if available.
# All variables set before this point can be overridden by users, by
# setting them directly in the defaults file. Use this to explicitly
# override these values, at your own risk.
if [ -f /etc/default/$NAME ] ; then
        . /etc/default/$NAME
fi

# Handle NUMA access to CPUs (SERVER-3574)
# This verifies the existence of numactl as well as testing that the command works
NUMACTL_ARGS="--interleave=all"
if which numactl &gt;/dev/null 2&gt;/dev/null &amp;&amp; numactl $NUMACTL_ARGS ls / &gt;/dev/null 2&gt;/dev/null
then
    NUMACTL="`which numactl` -- $NUMACTL_ARGS"
    DAEMON_OPTS=${DAEMON_OPTS:-"--config $CONF"}
else
    NUMACTL=""
    DAEMON_OPTS="-- "${DAEMON_OPTS:-"--config $CONF"}
fi


if test ! -x $DAEMON; then
    echo "Could not find $DAEMON"
    exit 0
fi

if test "x$ENABLE_MONGOD" != "xyes"; then
    exit 0
fi

. /lib/lsb/init-functions

STARTTIME=1
DIETIME=10                  # Time to wait for the server to die, in seconds
                            # If this value is set too low you might not
                            # let some servers to die gracefully and
                            # 'restart' will not work

DAEMONUSER=${DAEMONUSER:-mongodb}
DAEMONGROUP=${DAEMONGROUP:-mongodb}

set -e

running_pid() {
# Check if a given process pid's cmdline matches a given name
    pid=$1
    name=$2
    [ -z "$pid" ] &amp;&amp; return 1
    [ ! -d /proc/$pid ] &amp;&amp;  return 1
    cmd=`cat /proc/$pid/cmdline | tr "\000" "\n"|head -n 1 |cut -d : -f 1`
    # Is this the expected server
    [ "$cmd" != "$name" ] &amp;&amp;  return 1
    return 0
}

running() {
# Check if the process is running looking at /proc
# (works for all users)

    # No pidfile, probably no daemon present
    [ ! -f "$PIDFILE" ] &amp;&amp; return 1
    pid=`cat $PIDFILE`
    running_pid $pid $DAEMON || return 1
    return 0
}

start_server() {
            # Start the process using the wrapper
            start-stop-daemon --background --start --quiet --pidfile $PIDFILE \
                        --make-pidfile --chuid $DAEMONUSER:$DAEMONGROUP \
                        --exec $NUMACTL $DAEMON $DAEMON_OPTS
            errcode=$?
        return $errcode
}

stop_server() {
# Stop the process using the wrapper
            start-stop-daemon --stop --quiet --pidfile $PIDFILE \
                        --retry 300 \
                        --user $DAEMONUSER \
                        --exec $DAEMON
            errcode=$?
        return $errcode
}

force_stop() {
# Force the process to die killing it manually
        [ ! -e "$PIDFILE" ] &amp;&amp; return
        if running ; then
                kill -15 $pid
        # Is it really dead?
                sleep "$DIETIME"s
                if running ; then
                        kill -9 $pid
                        sleep "$DIETIME"s
                        if running ; then
                                echo "Cannot kill $NAME (pid=$pid)!"
                                exit 1
                        fi
                fi
        fi
        rm -f $PIDFILE
}


case "$1" in
  start)
        log_daemon_msg "Starting $DESC" "$NAME"
        # Check if it's running first
        if running ;  then
            log_progress_msg "apparently already running"
            log_end_msg 0
            exit 0
        fi
        if start_server ; then
            # NOTE: Some servers might die some time after they start,
            # this code will detect this issue if STARTTIME is set
            # to a reasonable value
            [ -n "$STARTTIME" ] &amp;&amp; sleep $STARTTIME # Wait some time
            if  running ;  then
                # It's ok, the server started and is running
                log_end_msg 0
            else
                # It is not running after we did start
                log_end_msg 1
            fi
        else
            # Either we could not start it
            log_end_msg 1
        fi
        ;;
  stop)
        log_daemon_msg "Stopping $DESC" "$NAME"
        if running ; then
            # Only stop the server if we see it running
                        errcode=0
            stop_server || errcode=$?
            log_end_msg $errcode
        else
            # If it's not running don't do anything
            log_progress_msg "apparently not running"
            log_end_msg 0
            exit 0
        fi
        ;;
  force-stop)
        # First try to stop gracefully the program
        $0 stop
        if running; then
            # If it's still running try to kill it more forcefully
            log_daemon_msg "Stopping (force) $DESC" "$NAME"
                        errcode=0
            force_stop || errcode=$?
            log_end_msg $errcode
        fi
        ;;
  restart|force-reload)
        log_daemon_msg "Restarting $DESC" "$NAME"
                errcode=0
        stop_server || errcode=$?
        # Wait some sensible amount, some server need this
        [ -n "$DIETIME" ] &amp;&amp; sleep $DIETIME
        start_server || errcode=$?
        [ -n "$STARTTIME" ] &amp;&amp; sleep $STARTTIME
        running || errcode=$?
        log_end_msg $errcode
        ;;
  status)

        log_daemon_msg "Checking status of $DESC" "$NAME"
        if running ;  then
            log_progress_msg "running"
            log_end_msg 0
        else
            log_progress_msg "apparently not running"
            log_end_msg 1
            exit 1
        fi
        ;;
  # MongoDB can't reload its configuration.
  reload)
        log_warning_msg "Reloading $NAME daemon: not implemented, as the daemon"
        log_warning_msg "cannot re-read the config file (use restart)."
        ;;

  *)
        N=/etc/init.d/$NAME
        echo "Usage: $N {start|stop|force-stop|restart|force-reload|status}" &gt;&amp;2
        exit 1
        ;;
esac

exit 0
    </code></pre>
</details>

<h3>Use “container-on-demand” to run MongoDB</h3>

<ul>
<li>Ask for container <code>Ubuntu 18.04 - MongoDB</code></li>
<li>Connect via SSH</li>
<li>Or via the WebTerminal</li>
<li>In the container, you should start MongoDB before playing with it:</li>
</ul>

<pre><code>$ service mongod start
* Starting database mongod                                              [ OK ]
$
$ cat 0-list_databases | mongo
MongoDB shell version v4.2.8
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&amp;gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("70f14b38-6d0b-48e1-a9a4-0534bcf15301") }
MongoDB server version: 4.2.8
admin   0.000GB
config  0.000GB
local   0.000GB
bye
$
</code></pre>


<!--==================================================-->
<br>

## Tasks
<details>
<summary>

### 0. List all databases
`mandatory`

File: [0-list_databases]()
</summary>

<p>Write a script that lists all databases in MongoDB.</p>

<pre><code>guillaume@ubuntu:~/0x01$ cat 0-list_databases | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
admin        0.000GB
config       0.000GB
local        0.000GB
logs         0.005GB
bye
guillaume@ubuntu:~/0x01$
</code></pre>


</details>

<details>
<summary>

### 1. Create a database
`mandatory`

File: [1-use_or_create_database]()
</summary>

<p>Write a script that creates or uses the database <code>my_db</code>:</p>

<pre><code>guillaume@ubuntu:~/0x01$ cat 0-list_databases | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
admin        0.000GB
config       0.000GB
local        0.000GB
logs         0.005GB
bye
guillaume@ubuntu:~/0x01$
guillaume@ubuntu:~/0x01$ cat 1-use_or_create_database | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
switched to db my_db
bye
guillaume@ubuntu:~/0x01$
</code></pre>


</details>

<details>
<summary>

### 2. Insert document
`mandatory`

File: [2-insert]()
</summary>

<p>Write a script that inserts a document in the collection <code>school</code>:</p>

<ul>
<li>The document must have one attribute <code>name</code> with value “Holberton school”</li>
<li>The database name will be passed as option of <code>mongo</code> command</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 2-insert | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
WriteResult({ "nInserted" : 1 })
bye
guillaume@ubuntu:~/0x01$
</code></pre>


</details>

<details>
<summary>

### 3. All documents
`mandatory`

File: [3-all]()
</summary>

<p>Write a script that lists all documents in the collection <code>school</code>:</p>

<ul>
<li>The database name will be passed as option of <code>mongo</code> command</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 3-all | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school" }
bye
guillaume@ubuntu:~/0x01$
</code></pre>


</details>

<details>
<summary>

### 4. All matches
`mandatory`

File: [4-match]()
</summary>

<p>Write a script that lists all documents with <code>name="Holberton school"</code> in the collection <code>school</code>:</p>

<ul>
<li>The database name will be passed as option of <code>mongo</code> command</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 4-match | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school" }
bye
guillaume@ubuntu:~/0x01$
</code></pre>


</details>

<details>
<summary>

### 5. Count
`mandatory`

File: [5-count]()
</summary>

<p>Write a script that displays the number of documents in the collection <code>school</code>:</p>

<ul>
<li>The database name will be passed as option of <code>mongo</code> command</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 5-count | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
1
bye
guillaume@ubuntu:~/0x01$
</code></pre>


</details>

<details>
<summary>

### 6. Update
`mandatory`

File: [6-update]()
</summary>

<p>Write a script that adds a new attribute to a document in the collection <code>school</code>:</p>

<ul>
<li>The script should update only document with <code>name="Holberton school"</code> (all of them)</li>
<li>The update should add the attribute <code>address</code> with the value “972 Mission street”</li>
<li>The database name will be passed as option of <code>mongo</code> command</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 6-update | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
bye
guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ cat 4-match | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school", "address" : "972 Mission street" }
bye
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 7. Delete by match
`mandatory`

File: [7-delete]()
</summary>

<p>Write a script that deletes all documents with <code>name="Holberton school"</code> in the collection <code>school</code>:</p>

<ul>
<li>The database name will be passed as option of <code>mongo</code> command</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 7-delete | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "acknowledged" : true, "deletedCount" : 1 }
bye
guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ cat 4-match | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
bye
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 8. List all documents in Python
`mandatory`

File: [8-all.py]()
</summary>

<p>Write a Python function that lists all documents in a collection:</p>

<ul>
<li>Prototype: <code>def list_all(mongo_collection):</code></li>
<li>Return an empty list if no document in the collection</li>
<li><code>mongo_collection</code> will be the <code>pymongo</code> collection object</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 8-main.py
#!/usr/bin/env python3
""" 8-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school
    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {}".format(school.get('_id'), school.get('name')))

guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ ./8-main.py
[5a8f60cfd4321e1403ba7ab9] Holberton school
[5a8f60cfd4321e1403ba7aba] UCSD
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 9. Insert a document in Python
`mandatory`

File: [9-insert_school.py]()
</summary>

<p>Write a Python function that inserts a new document in a collection based on <code>kwargs</code>:</p>

<ul>
<li>Prototype: <code>def insert_school(mongo_collection, **kwargs):</code></li>
<li><code>mongo_collection</code> will be the <code>pymongo</code> collection object</li>
<li>Returns the new <code>_id</code></li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 9-main.py
#!/usr/bin/env python3
""" 9-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all
insert_school = __import__('9-insert_school').insert_school

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school
    new_school_id = insert_school(school_collection, name="UCSF", address="505 Parnassus Ave")
    print("New school created: {}".format(new_school_id))

    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('address', "")))

guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ ./9-main.py
New school created: 5a8f60cfd4321e1403ba7abb
[5a8f60cfd4321e1403ba7ab9] Holberton school
[5a8f60cfd4321e1403ba7aba] UCSD
[5a8f60cfd4321e1403ba7abb] UCSF 505 Parnassus Ave
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 10. Change school topics
`mandatory`

File: [10-update_topics.py]()
</summary>

<p>Write a Python function that changes all topics of a school document based on the name:</p>

<ul>
<li>Prototype: <code>def update_topics(mongo_collection, name, topics):</code></li>
<li><code>mongo_collection</code> will be the <code>pymongo</code> collection object</li>
<li><code>name</code> (string) will be the school name to update</li>
<li><code>topics</code> (list of strings) will be the list of topics approached in the school</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 10-main.py
#!/usr/bin/env python3
""" 10-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all
update_topics = __import__('10-update_topics').update_topics

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school
    update_topics(school_collection, "Holberton school", ["Sys admin", "AI", "Algorithm"])

    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('topics', "")))

    update_topics(school_collection, "Holberton school", ["iOS"])

    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('topics', "")))

guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ ./10-main.py
[5a8f60cfd4321e1403ba7abb] UCSF 
[5a8f60cfd4321e1403ba7aba] UCSD 
[5a8f60cfd4321e1403ba7ab9] Holberton school ['Sys admin', 'AI', 'Algorithm']
[5a8f60cfd4321e1403ba7abb] UCSF 
[5a8f60cfd4321e1403ba7aba] UCSD 
[5a8f60cfd4321e1403ba7ab9] Holberton school ['iOS']
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 11. Where can I learn Python?
`mandatory`

File: [11-schools_by_topic.py]()
</summary>

<p>Write a Python function that returns the list of school having a specific topic:</p>

<ul>
<li>Prototype: <code>def schools_by_topic(mongo_collection, topic):</code></li>
<li><code>mongo_collection</code> will be the <code>pymongo</code> collection object</li>
<li><code>topic</code> (string) will be topic searched</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 11-main.py
#!/usr/bin/env python3
""" 11-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all
insert_school = __import__('9-insert_school').insert_school
schools_by_topic = __import__('11-schools_by_topic').schools_by_topic

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school

    j_schools = [
        { 'name': "Holberton school", 'topics': ["Algo", "C", "Python", "React"]},
        { 'name': "UCSF", 'topics': ["Algo", "MongoDB"]},
        { 'name': "UCLA", 'topics': ["C", "Python"]},
        { 'name': "UCSD", 'topics': ["Cassandra"]},
        { 'name': "Stanford", 'topics': ["C", "React", "Javascript"]}
    ]
    for j_school in j_schools:
        insert_school(school_collection, **j_school)

    schools = schools_by_topic(school_collection, "Python")
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('topics', "")))

guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ ./11-main.py
[5a90731fd4321e1e5a3f53e3] Holberton school ['Algo', 'C', 'Python', 'React']
[5a90731fd4321e1e5a3f53e5] UCLA ['C', 'Python']
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 12. Log stats
`mandatory`

File: [12-log_stats.py]()
</summary>

<p>Write a Python script that provides some stats about Nginx logs stored in MongoDB:</p>

<ul>
<li>Database: <code>logs</code></li>
<li>Collection: <code>nginx</code></li>
<li>Display (same as the example):

<ul>
<li>first line: <code>x logs</code> where <code>x</code> is the number of documents in this collection</li>
<li>second line: <code>Methods:</code></li>
<li>5 lines with the number of documents with the <code>method</code> = <code>["GET", "POST", "PUT", "PATCH", "DELETE"]</code> in this order (see example below - warning: it’s a tabulation before each line) </li>
<li>one line with the number of documents with:

<ul>
<li><code>method=GET</code></li>
<li><code>path=/status</code></li>
</ul></li>
</ul></li>
</ul>

<p>You can use this dump as data sample: <a href="https://intranet.alxswe.com/rltoken/0szbpslKvH3RqKb_2HUeoQ" target="_blank" title="dump.zip">dump.zip</a> </p>

<p>The output of your script <strong>must be exactly the same as the example</strong></p>

<pre><code>guillaume@ubuntu:~/0x01$ curl -o dump.zip -s "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-webstack/411/dump.zip"
guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ unzip dump.zip
Archive:  dump.zip
   creating: dump/
   creating: dump/logs/
  inflating: dump/logs/nginx.metadata.json  
  inflating: dump/logs/nginx.bson    
guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ mongorestore dump
2018-02-23T20:12:37.807+0000    preparing collections to restore from
2018-02-23T20:12:37.816+0000    reading metadata for logs.nginx from dump/logs/nginx.metadata.json
2018-02-23T20:12:37.825+0000    restoring logs.nginx from dump/logs/nginx.bson
2018-02-23T20:12:40.804+0000    [##......................]  logs.nginx  1.21MB/13.4MB  (9.0%)
2018-02-23T20:12:43.803+0000    [#####...................]  logs.nginx  2.88MB/13.4MB  (21.4%)
2018-02-23T20:12:46.803+0000    [#######.................]  logs.nginx  4.22MB/13.4MB  (31.4%)
2018-02-23T20:12:49.803+0000    [##########..............]  logs.nginx  5.73MB/13.4MB  (42.7%)
2018-02-23T20:12:52.803+0000    [############............]  logs.nginx  7.23MB/13.4MB  (53.8%)
2018-02-23T20:12:55.803+0000    [###############.........]  logs.nginx  8.53MB/13.4MB  (63.5%)
2018-02-23T20:12:58.803+0000    [#################.......]  logs.nginx  10.1MB/13.4MB  (74.9%)
2018-02-23T20:13:01.803+0000    [####################....]  logs.nginx  11.3MB/13.4MB  (83.9%)
2018-02-23T20:13:04.803+0000    [######################..]  logs.nginx  12.8MB/13.4MB  (94.9%)
2018-02-23T20:13:06.228+0000    [########################]  logs.nginx  13.4MB/13.4MB  (100.0%)
2018-02-23T20:13:06.230+0000    no indexes to restore
2018-02-23T20:13:06.231+0000    finished restoring logs.nginx (94778 documents)
2018-02-23T20:13:06.232+0000    done
guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ ./12-log_stats.py 
94778 logs
Methods:
    method GET: 93842
    method POST: 229
    method PUT: 0
    method PATCH: 0
    method DELETE: 0
47415 status check
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 13. Regex filter
`#advanced`

File: [100-find]()
</summary>

<p>Write a script that lists all documents with <code>name</code> starting by <code>Holberton</code> in the collection <code>school</code>:</p>

<ul>
<li>The database name will be passed as option of <code>mongo</code> command</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 100-find | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a90731fd4321e1e5a3f53e3"), "name" : "Holberton school" }
{ "_id" : ObjectId("5a90731fd4321e1e5a3f53e3"), "name" : "Holberton School" }
{ "_id" : ObjectId("5a90731fd4321e1e5a3f53e3"), "name" : "Holberton-school" }
bye
guillaume@ubuntu:~/0x01$
</code></pre>


</details>

<details>
<summary>

### 14. Top students
`#advanced`

File: [101-students.py]()
</summary>

<p>Write a Python function that returns all students sorted by average score:</p>

<ul>
<li>Prototype: <code>def top_students(mongo_collection):</code></li>
<li><code>mongo_collection</code> will be the <code>pymongo</code> collection object</li>
<li>The top must be ordered</li>
<li>The average score must be part of each item returns with key = <code>averageScore</code></li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ cat 101-main.py
#!/usr/bin/env python3
""" 101-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all
insert_school = __import__('9-insert_school').insert_school
top_students = __import__('101-students').top_students

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    students_collection = client.my_db.students

    j_students = [
        { 'name': "John", 'topics': [{ 'title': "Algo", 'score': 10.3 },{ 'title': "C", 'score': 6.2 }, { 'title': "Python", 'score': 12.1 }]},
        { 'name': "Bob", 'topics': [{ 'title': "Algo", 'score': 5.4 },{ 'title': "C", 'score': 4.9 }, { 'title': "Python", 'score': 7.9 }]},
        { 'name': "Sonia", 'topics': [{ 'title': "Algo", 'score': 14.8 },{ 'title': "C", 'score': 8.8 }, { 'title': "Python", 'score': 15.7 }]},
        { 'name': "Amy", 'topics': [{ 'title': "Algo", 'score': 9.1 },{ 'title': "C", 'score': 14.2 }, { 'title': "Python", 'score': 4.8 }]},
        { 'name': "Julia", 'topics': [{ 'title': "Algo", 'score': 10.5 },{ 'title': "C", 'score': 10.2 }, { 'title': "Python", 'score': 10.1 }]}
    ]
    for j_student in j_students:
        insert_school(students_collection, **j_student)

    students = list_all(students_collection)
    for student in students:
        print("[{}] {} - {}".format(student.get('_id'), student.get('name'), student.get('topics')))

    top_students = top_students(students_collection)
    for student in top_students:
        print("[{}] {} =&gt; {}".format(student.get('_id'), student.get('name'), student.get('averageScore')))

guillaume@ubuntu:~/0x01$ 
guillaume@ubuntu:~/0x01$ ./101-main.py
[5a90776bd4321e1ec94fc408] John - [{'title': 'Algo', 'score': 10.3}, {'title': 'C', 'score': 6.2}, {'title': 'Python', 'score': 12.1}]
[5a90776bd4321e1ec94fc409] Bob - [{'title': 'Algo', 'score': 5.4}, {'title': 'C', 'score': 4.9}, {'title': 'Python', 'score': 7.9}]
[5a90776bd4321e1ec94fc40a] Sonia - [{'title': 'Algo', 'score': 14.8}, {'title': 'C', 'score': 8.8}, {'title': 'Python', 'score': 15.7}]
[5a90776bd4321e1ec94fc40b] Amy - [{'title': 'Algo', 'score': 9.1}, {'title': 'C', 'score': 14.2}, {'title': 'Python', 'score': 4.8}]
[5a90776bd4321e1ec94fc40c] Julia - [{'title': 'Algo', 'score': 10.5}, {'title': 'C', 'score': 10.2}, {'title': 'Python', 'score': 10.1}]
[5a90776bd4321e1ec94fc40a] Sonia =&gt; 13.1
[5a90776bd4321e1ec94fc40c] Julia =&gt; 10.266666666666666
[5a90776bd4321e1ec94fc408] John =&gt; 9.533333333333333
[5a90776bd4321e1ec94fc40b] Amy =&gt; 9.366666666666665
[5a90776bd4321e1ec94fc409] Bob =&gt; 6.066666666666667
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

<details>
<summary>

### 15. Log stats - new version
`#advanced`

File: [102-log_stats.py ]()
</summary>

<p>Improve <code>12-log_stats.py</code> by adding the top 10 of the most present IPs in the collection <code>nginx</code> of the database <code>logs</code>:</p>

<ul>
<li>The IPs top must be sorted (like the example below)</li>
</ul>

<pre><code>guillaume@ubuntu:~/0x01$ ./102-log_stats.py 
94778 logs
Methods:
    method GET: 93842
    method POST: 229
    method PUT: 0
    method PATCH: 0
    method DELETE: 0
47415 status check
IPs:
    172.31.63.67: 15805
    172.31.2.14: 15805
    172.31.29.194: 15805
    69.162.124.230: 529
    64.124.26.109: 408
    64.62.224.29: 217
    34.207.121.61: 183
    47.88.100.4: 166
    45.249.84.250: 160
    216.244.66.228: 150
guillaume@ubuntu:~/0x01$ 
</code></pre>


</details>

