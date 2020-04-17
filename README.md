
## Recursive GoIndex Downloader by atlonxp

This code was created and improved by adapting the code from pankaj260 https://colab.research.google.com/drive/1tmsLGuswIZIZ_oM35EMW8TbJ6pQPt1rY#scrollTo=3bCnUMUg_SoT&forceEdit=true&sandboxMode=true

**Features**
*   Recursive crawler (atlonxp)
*   Download all folders and files in a given url (atlonxp)
*   Download all folders and files in in sub-folders (atlonxp)
*   Adaptive delay in fetching url (atlonxp)
*   Store folders/files directly to your Google Drive (pankaj260)
*   Folders and files exclusion filters
*   Download queue supported
*   Auto-domain URL detection
*   API-based GoIndex crawler
*   Parallel/Multiple files downloader

**Version 2**:

API-based crawler with paralled files downloader
	
	17 April 2020 (v2.1)

	+ fixed URL duplicated when crawling
	+ added search 'files' key for some websites do not have proper files structure. So, we search it\
	
	16 April 2020

	+ crawler_v2:
		* API-based GoIndex crawler
		* Collecting all urls to be downloaded
	+ parallel downloader
		* TDQM progress bar

**Version 1**:

Simple HTTP-based crawler and simple series downloader

	15 April 2020
	-   Added auto-domain URL detection
	-   Added simple download queue

	14 April 2020
		-   initial
