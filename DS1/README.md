<B> About : </B>
<p> This repository contains musical data in RDF format and the different SILK linking configuration files. It is organized in the following four directories: </p>
<ol>
<li> MARCXML : contains INTERMARC-XML records from BNF (Bibliothèque Nationale de France) and UNIMARC-XML records from PP (Philharmonie de Paris). </li>
<li> RDF: contains the correpsonding RDF files of these records (in the folder “MARCXML”). The MARC-XML records were converted using the prototype MARC2RDF (work in progress) which is based on the DOREMUS model. In addition, a display in MARC (MAchine Readable Cataloging) format is an option of this prototype to view an INTERMARC-XML or an UNIMARC-XML file in MARC format (for more details: https://github.com/DOREMUS-ANR/marc2rdf ). </li>
<li> RefAlign: contains “ref-OAEI” file specifying the matching pairs between the works in the BNF dataset and the works in the PP dataset. It aims at evaluating the interlinking tools in terms of ability to detect heterogeneities identified between these works. Different files named “ref-hi” (1<= i <= 10), in the folder “HetReferences”, indicate the match pairs having the heterogeneity “hi” as follows: 
<ol>
<li> H1: indicates the presence of letters and numbers in the title of the work. </li>
<li> H2: orthographic differences. </li>
<li> H3: the works do not have a catalog/opus number. </li>
<li> H5: the titles of the works are multilingual. </li>
<li> H6: the description of a work contains diacritical characters. </li>
<li> H7: property depth heterogeneity:  a property can be specified directly through a literal value while in another dataset the same information is given by a longer property chain including several triples. </li>
<li> H8: the same information across two instances is described by different properties. </li>
<li> H9: an instance can be described by more properties in one dataset than  in the other. </li>
<li> H10: at least one of the two instances has no title. </li>
</ol>
</li>
<li> SILK configurations: contains two configuration files:
<ol>
<li>  “config1” file: SILK compares the works over all their properties. </li>
<li>  “config2” file: SILK compares the works only over their titles. </li>
</ol>
To download SILK:
https://github.com/silk-framework/silk/releases/download/release-2.7.1/silk-workbench-2.7.1.tgz
Command line to execute SILK: java -DconfigFile=<configuration file path> -jar silk.jar
</li>
</ol>