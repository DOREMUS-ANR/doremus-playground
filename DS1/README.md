<B> <u> About : </u> </B>
<p> This repository contains musical data in RDF format and the different SILK linking configuration files. It is organized in the following four directories: </p>
<ol>
<li> <u> MARCXML </u>: contains INTERMARC-XML records from BNF (Bibliothèque Nationale de France) and UNIMARC-XML records from PP (Philharmonie de Paris). </li>
<li> <u> RDF </u>: contains the correpsonding RDF files of these records (in the folder “MARCXML”). The MARC-XML records were converted using the prototype MARC2RDF (work in progress) which is based on the DOREMUS model. In addition, a display in MARC (MAchine Readable Cataloging) format is an option of this prototype to view an INTERMARC-XML or an UNIMARC-XML file in MARC format (for more details: https://github.com/DOREMUS-ANR/marc2rdf ). </li>
<li> <u> RefAlign </u>: contains “ref-OAEI” file specifying the matching pairs between the works in the BNF dataset and the works in the PP dataset. It aims at evaluating the interlinking tools in terms of ability to detect heterogeneities identified between these works. Different files named “ref-hi” (1<= i <= 10), in the folder “HetReferences”, indicate the match pairs having the heterogeneity “hi” as follows: 
<ol>
<li> <u> H1 </u>: indicates the presence of letters and numbers in the title of the work. </li>
<li> <u> H2 </u>: orthographic differences. </li>
<li> <u> H3 </u>: the works do not have a catalog/opus number. </li>
<li> <u> H5 </u>: the titles of the works are multilingual. </li>
<li> <u> H6 </u>: the description of a work contains diacritical characters. </li>
<li> <u> H7 </u>: property depth heterogeneity:  a property can be specified directly through a literal value while in another dataset the same information is given by a longer property chain including several triples. </li>
<li> <u> H8 </u>: the same information across two instances is described by different properties. </li>
<li> <u> H9 </u>: an instance can be described by more properties in one dataset than  in the other. </li>
<li> <u> H10 </u>: at least one of the two instances has no title. </li>
</ol>
</li>
<li> <u> SILK configurations </u>: contains two configuration files:
<ol>
<li>  <u> “config1” file </u>: SILK compares the works over all their properties. </li>
<li>  <u> “config2” file </u>: SILK compares the works only over their titles. </li>
</ol>
<u> To download SILK </u>:
https://github.com/silk-framework/silk/releases/download/release-2.7.1/silk-workbench-2.7.1.tgz
<u> Command line to execute SILK </u>: java -DconfigFile=<configuration file path> -jar silk.jar
</li>
</ol>