**Predicting Coupon Redemption**

XYZ Credit Card company regularly helps its merchants understand their data better and make key business decisions accurately by 
providing machine learning and analytics consulting. ABC is an established Brick & Mortar retailer that frequently conducts 
marketing campaigns for its diverse product range. As a merchant of XYZ, they have sought XYZ to assist them in their discount marketing 
process using the power of machine learning. Can you wear an expert hat and help out ABC?

 

Discount marketing and coupon usage are very widely used promotional techniques to attract new customers and to retain & reinforce 
the loyalty of existing customers. Measuring a consumer’s propensity towards coupon usage and predicting redemption behaviour 
are crucial parameters in assessing the effectiveness of a marketing campaign.

 
![image](https://github.com/user-attachments/assets/fb0d2591-cfdb-4d14-9af1-4a5fef43a024)


Data dictionary
 

**train.csv**: Train data containing the coupons offered to the given customers under the 18 campaigns

| **Variable**         | **Definition**                                                                 |
|----------------------|--------------------------------------------------------------------------------|
| `id`                 | Unique ID for coupon customer impression                                       |
| `campaign_id`        | Unique ID for a discount campaign                                              |
| `coupon_id`          | Unique ID for a discount coupon                                                |
| `customer_id`        | Unique ID for a customer                                                       |
| `redemption_status`  | (target) Redemption status (0 - Coupon not redeemed, 1 - Coupon redeemed)      |


campaign_data.csv: Campaign information for each of the 28 campaigns
| **Variable**      | **Definition**                                 |
|-------------------|------------------------------------------------|
| `campaign_id`     | Unique ID for a discount campaign              |
| `campaign_type`   | Anonymised campaign type (`X` or `Y`)          |
| `start_date`      | Campaign start date                            |
| `end_date`        | Campaign end date                              |


coupon_item_mapping.csv: Mapping of coupon and items valid for discount under that coupon

| **Variable**   | **Definition**                                                                 |
|----------------|--------------------------------------------------------------------------------|
| `coupon_id`    | Unique ID for a discount coupon (no specific order)                            |
| `item_id`      | Unique ID for items for which the given coupon is valid (no specific order)    |

 
customer_demographics.csv: Customer demographic information for some customers
| **Variable**       | **Definition**                                                                 |
|--------------------|--------------------------------------------------------------------------------|
| `customer_id`      | Unique ID for a customer                                                       |
| `age_range`        | Age range of customer family in years                                          |
| `marital_status`   | Marital status of the customer (`Married` or `Single`)                         |
| `rented`           | Accommodation status (`0` - not rented, `1` - rented)                          |
| `family_size`      | Number of family members                                                       |
| `no_of_children`   | Number of children in the family                                               |
| `income_bracket`   | Label-encoded income bracket (higher number = higher income)                   |

 
customer_transaction_data.csv: Transaction data for all customers for the duration of campaigns in the train data

| **Variable**        | **Definition**                                                                          |
|---------------------|------------------------------------------------------------------------------------------|
| `date`              | Date of transaction                                                                     |
| `customer_id`       | Unique ID for a customer                                                                |
| `item_id`           | Unique ID for item                                                                      |
| `quantity`          | Quantity of items bought                                                                |
| `selling_price`     | Sales value of the transaction                                                          |
| `other_discount`    | Discount from other sources (e.g., manufacturer coupon, loyalty card)                   |
| `coupon_discount`   | Discount availed from retailer coupon                                                   |

 
item_data.csv: Item information for each item sold by the retailer
| **Variable**   | **Definition**                                             |
|----------------|------------------------------------------------------------|
| `item_id`      | Unique ID for item                                         |
| `brand`        | Unique ID for item brand                                   |
| `brand_type`   | Brand type (`Local` or `Established`)                      |
| `category`     | Item category                                              |

 
test.csv: Contains the coupon customer combination for which redemption status is to be predicted

| **Variable**   | **Definition**                                |
|----------------|-----------------------------------------------|
| `id`           | Unique ID for coupon customer impression      |
| `campaign_id`  | Unique ID for a discount campaign             |
| `coupon_id`    | Unique ID for a discount coupon               |
| `customer_id`  | Unique ID for a customer                      |

 



 

sample_submission.csv: This file contains the format in which you have to submit your predictions.
