

## Install solr version 4.10.4 for BioPortal

* Download the archive
```bash
wget http://archive.apache.org/dist/lucene/solr/4.10.4/solr-4.10.4.tgz
tar -xvf solr-4.10.4.tgz
```

* We will use the solr example. Copy it somewhere where it will be easily found (it will be the `SOLR_HOME`). Here we put it in /opt/solr.

```bash
cp -R solr-4.10.4/example /opt/solr
```
* Get the solr config used for BioPortal. By putting the content of this git repository in /opt/solr/solr
It will define the different cores used by solr

```bash
cd /opt/solr
git clone https://gite.lirmm.fr/vemonet/bioportal-solr.git solr
```

## Run solr

Run on http://localhost:8983/solr/

```bash
cd /opt/solr
java -Dsolr.solr.home=solr -jar start.jar
```
