This is a simple SBT plugin which can rewrite the markdown files in _base_``/tutorial`` directory to HTML in a suitable format.

If you add ``addSbtPlugin("org.eigengo" % "sbt-mdrw" % "1.0.0-SNAPSHOT")`` to your ``~/.sbt/0.13/plugins.sbt``, 
every project you use will include the ``mdrw`` command; if you do not want system-wide plugin, add the plugin only to
the projects that require it. 

The parameter of the ``mdrw`` command can be the name of the rewriter; currently, I support ``activator`` and ``wordpress``. 
As you can imagine, the ``activator`` generates HTML suitable for the Typesafe Activator, ``wordpress`` generates HTML 
suitable for Wordpress.

---

For sample usage, check out the [Akka & Cassandra Activator](https://github.com/eigengo/activator-akka-cassandra). The
``tutorial/index.html`` file was generated from ``tutorial/index.md`` by running ``sbt mdrw activator``. The
