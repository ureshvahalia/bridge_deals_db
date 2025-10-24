# bridge_deals_db  
DB of bridge team games scraped from BBO and other repositories, along with analytics derived from these deals  
The repository has the following files:  
bridge_deals.tar.gz: gzipped tar file with all the deals, organized by file type, then by year and event.  
  -- LIN files are from BBO vugraphs. I have gathered all files from 2020 to April 2025  
  -- RBN files are from Richard Pavlicek's collection (don't think it is available online anymore)  
  -- JSON files are from Wojitek Balcerak's collection (https://balcerak.de/bridge/downloads.html)  
  -- PBN files are from a variety of sources including github  
RawDB: Folder with all the deals extracted from the respective formats and stored as csv files. This contains:  
  -- RawData.csv All ingested records with minimal processing  
  -- all.csv: Flat file with all data and validation flags  
  -- events.csv: Unique events and matches  
  -- deals.csv Unique deals (hands + dealer + vulnerability + match)  
  -- boards.csv Individual board records (one per deal per table)  
  -- hands.csv Unique hand combinations with analysis  
  -- ProcessedDeals.csv Deals with derived hand features  
  -- ProcessedBoards.csv Boards with validated and derived auction/contract data plus double-dummy results  
Analysis: Folder with results of analysis of these deals. This contains:  
  -- FullBoards.csv: One row per board with all derived board-specific features  
  -- FullDeals.csv: One row per deal with results of both tables side-by-side and all derived features  
  -- Summary.csv: Key summary results from the analysis  
  -- Openings.csv: Analysis of opening bids and their outcome  
  -- EarlyBids.csv: Analysis of competitive situations where one table opens and the other does not  
