# o-gauge-price-prediction

Price prediction system for O-gauge model locomotives built using eBay API data and machine learning in Python.

1. Problem:
   - O gauge locomotives only
   - eBay sold listings only\*\*
     - Unable to do this with newer eBay API, so using current listings
   - Brands: Lionel, MTH, Atlas O

2. Target variable:
   - Final sold price excluding shipping
   - Auctions or buy now
   - Exclude lots, only focus on single locomotive listings

3. Initial features
   - Required:
     - Sold price
     - Brand
     - Condition
     - Digital / conventional control
     - With / without sound
     - Listing title
   - Possible additions:
     - Seller feedback
     - With / without box
     - Other keywords

4. Data scraping:
   - eBay API
   - 1000 listings
   - One-time initial scrape

5. Initial dataset columns:
   - sold_price
   - brand
   - condition
   - control_type
   - has_sound
   - title_text
   - sold_date

6. Data cleaning:
   - Initial rules:
     - Remove prices under realistic threshold
     - Standardize condition labels
     - Normalize brand naming
     - Remove other scales (HO, G) produced by given brands
     - Drop listings with missing price or title
   - Possible additions:
     - Distinguish between brand lines (ex. MTH Premier/Railking)

7. Final goal:
   - Cleaned dataset
   - Trained model
