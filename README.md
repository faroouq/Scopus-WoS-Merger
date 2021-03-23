# Scopus-WoS-Merger
The repository consist of Python code that allow users to merger downloaded search results from Scopus and Wos.

It contains two jupyter notebooks containing Python code:
- ScopusWoSComparator.ipynb, and
- dbCreator.ipynb

## Scopus WoS Comparator (ScopusWoSComparator.ipynb)
This code takes a co-located file of exported search results from Scopus and Web of Science (WoS). The files should be named <i><b>"scopus_title_keyword_abstract_tab.csv"</i></b> and <i><b>"wos_full_record.csv"</i></b>, respectively.

Then the code merges these files, while removing useless information like citation of a proceeding, counting the papers that appear in one list but not the other, and counting those that appear in both.

Finally, the application saves a combined list of peprs (without duplication) in a co-located file called <i><b>"papersToRead.txt"</i></b> and the results that are presumed to not be scientific papers as saved in <i><b>"bad.txt"</i></b>.

## DB Creator (dbCreator.ipynb)
This Python code depends on the "ScopusWoSComparator.ipynb". It takes the file <i><b>"papersToRead.txt"</i></b> generated by the aforementioned notebook and the other two co-located files <i><b>"scopus_title_keyword_abstract_tab.csv"</i></b> and <i><b>"wos_full_record.csv"</i></b>, which were search results exported from Scopus and Web of Science (WoS), respectively.

Db Creator merges the two document and develop a Scopus-like csv file that can be used by <a href="https://www.vosviewer.com/">VOSviewer</a>. The resulting file is created in the smae folder with the jupyter notebook and it is named <i><b>"idsPapersDataset.csv"</i></b>.

## Other Files
- <b>thesaurus_fog.txt</b>: This is a file that tells VOSviewer plurality of words that mean the same thing and that they should be counded as one.
- <b>idsPapersDataset.csv</b>: This file is a merged database, which contained both Scopus and WoS search results. It can be used directly with VOSviewer.
- <b>papersToRead.txt</b>: This file contains a non-duplicate list of scientific papers from both Scopus and WOS.
- <b>bad.txt</b>: This file contains a list of titles the Python code think are not papers. This is common with Scopus search result, which list title of proceedings in search results.
- <b>search_term.txt</b>: Contains the search term used in out survey paper titled, "A Comprehensive Survey of Intrusion Detectionand Prevention Systems in Fog Computing"

## Bibtex
@misc{aliyu2021merger,  
    url={https://github.com/faroouq/Scopus-WoS-Merger},  
    author={Frouq, Aliyu},  
    year={2021},  
    month={January},  
    title={Scopus-WoS-Merger},  
    note={Accessed on 1st January, 2021}  
}

Don't forget to cite this work
