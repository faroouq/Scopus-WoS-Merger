# Scopus-WoS-Merger
The repository consist of Python code that allow users to merger downloaded search results from Scopus and Wos.

It contains two jupyter notebooks containing Python code:
-ScopusWoSComparator.ipynb, and
-dbCreator.ipynb

## Scopus WoS Comparator (ScopusWoSComparator.ipynb)
This code takes a co-located file of exported search results from Scopus and Web of Science (WoS). The files should be named "scopus_title_keyword_abstract_tab.csv" and "wos_full_record.csv", respectively.

Then the code merges these files, while removing useless information like citation of a proceeding, counting the papers that appear in one list but not the other, and counting those that appear in both.

Finally, the application saves a combined list of peprs (without duplication) in a co-located file called "papersToRead.txt and the results that are presumed to not be scientific papers as saved in "bad.txt"

