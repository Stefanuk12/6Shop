# Goal 
A delivery service for sixth form students (and teachers?)

# More
Designed to be adopted at a large scale, which reuslts in fast speeds and a great user experience.

# Technologies used
- Database: ScyllaDB
- Payment: Square
- Frontend: Svelte
- Backend: Rust

# Register Process
- Users make an account
- Attach a school
- Photo ID to verify user
- (Optional) Link payment method + verify payment method

# Order Process
- Select a store brand
- If there is more than one store (e.g., 2 co-ops), ask user to select one
- Web scrape top products, only showing in stock ones
- Make sure a "delivery person" is "online"
- Users add products to cart
    - Support for to order from many stores at once?
- Checkout

# Delivery Process
- Order recieved
- Assign to a deliveree
    - Alternative could be deliveree picks their orders to fulful (depending on deliveree, they can choose)
- Deliveree fulfils order and goes to customer
- Customer scans barcode in app to confirm delivery
- Deliveree gets confirmation on app
- Customer recieves items

# Costs
- Base price is the cost of the products
- Founders get a fixed 5% fee with a minimum 10p, labelled as service fee
- Deliveree get a fixed £0.75+? per order (more depending on distance), labelled as delivery fee
- e.g., £5.00 order -> £5.00 + £0.25 + £0.75 -> £5.75
    - `fullTotal = 0.75 + total + clamp(0.10, total, total * 0.05)`