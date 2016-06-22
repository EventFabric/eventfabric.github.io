
to install analytics and disqus extensions for sphinx::

    hg clone https://bitbucket.org/marianoguerra/sphinx-contrib/
    cd sphinx-contrib/googleanalytics
    sudo python3 setup.py install

    cd ../disqus
    sudo python3 setup.py install

    sudo apt install python3-sphinxcontrib.youtube

you may have to change the line::

    return "; ".join(sorted("%s: %s" % kv for kv in d.iteritems()))

in dist-packages/sphinxcontrib/youtube.py to::

    return "; ".join(sorted("%s: %s" % kv for kv in d.items()))
