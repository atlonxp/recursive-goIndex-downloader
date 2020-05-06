
## Recursive GoIndex Downloader by atlonxp

### Features
*   Recursive crawler (**atlonxp**)
*   Download all folders and files in a given url (**atlonxp**)
*   Download all folders and files in in sub-folders (**atlonxp**)
*   Adaptive delay in fetching url (**atlonxp**)
*   Store folders/files directly to your Google Drive (**pankaj260**)
*   Folders and files exclusion filters (**atlonxp**)
*   Download queue supported (**atlonxp**)
*   Auto-domain URL detection (**atlonxp**)
*   API-based GoIndex crawler (**atlonxp**, **ifvv**)
*   Parallel/Multiple files downloader (**atlonxp**)
*   Auto-skip password-protected folders (**cxu-fork**)


### Upcoming 
*   parallel crawlers

### Version 2:

API-based crawler with parallel files downloader
	
	28 April 2020 (v2.4.0)
	
	+ added feature: curl download mode as default (we found sometime, requests.get caused a corrupted file)
	+ added feature: file size check. If not the same in the metadata, we force download
	+ added feature: double file size check. Once a file is downloaded, we re-check the it size with the metdadata
	+ revised time delay while crawling and downloading 
	+ fixed major bugs when checking file size
	
	26 April 2020 (v2.3.3)

	+ added downloaded size information
	
	22 April 2020 (v2.3.2)
    ---------------------
	
	+ added summary
	+ added Exception when file is unable to download
	
	21 April 2020 (v2.3.1)
	---------------------
	While crawling, fetching might cause errors sometime due to some quick requests or server is busy.
	This problem has caused the eror in getting a json, so we re-fetch the url again (up to MAX_RETRY_CRAWLING)
	or until we found key "files" in the return response. Once retries is reached the maximum and
	the key "files" is not found, so we ignore this link (return [])

	At the end, if you find there is failure, just re-run the download section again. Unless you set
	OVERWITE = TRUE, all files will be re-downloaded

	+ added MAX_RETRY_CRAWLING (v2.3)
	+ fixed FILE_EXISTING_CHECK (stupid) bug
	+ added failure-links download task
	
	20 April 2020 (v2.2)
	---------------------
	Some sub-folders may be password-protected which will cause the error while crawling, so we skip this folder
	
	+ added auto-skip password-protected folder
	
	17 April 2020 (v2.1)
    ---------------------
	+ fixed URL duplicated when crawling
	+ added search 'files' key for some websites do not have proper files structure. So, we search it\
	
	16 April 2020 (v2.0)
    ---------------------
	+ crawler_v2:
		* API-based GoIndex crawler
		* Collecting all urls to be downloaded
	+ parallel downloader
		* TDQM progress bar

### Version 1:

Simple HTTP-based crawler and simple series downloader

Version 1 was created and improved by adapting the code from pankaj260 https://colab.research.google.com/drive/1tmsLGuswIZIZ_oM35EMW8TbJ6pQPt1rY#scrollTo=3bCnUMUg_SoT&forceEdit=true&sandboxMode=true


	15 April 2020 (v1.1)
	---------------------
	-   Added auto-domain URL detection
	-   Added simple download queue

	14 April 2020 (v1.0)
	---------------------
    -   initial
