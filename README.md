# Snack Tracker App
http://snackers.s3-website-us-east-1.amazonaws.com/

** To explore the app, you need to make an account with a valid email address. **

  This app was an orientation project made during the first week of my summer 2019 internship at Ridgeline. Although unrelated to the company's product and my summer assignment, it was a creative way for interns to become familiar with AWS and the technologies used at the company. 
  
  Snack Tracker is a way to manage the snack program in the office, by allowing individuals to track their office snack consumption and allowing the company to view aggregate snack consumption data. The code in the app is my own, besides the "Ridgeline Snacks" page, which was the work of my parter.
  
  From AWS, this app uses DynamoDB, Cognito, IAM, and S3. The app structure is loosely based on this tutorial https://serverless-stack.com/, as this tutorial is how we were introduced to AWS. 

## Key features to note by page

### Add Snack
**Item input**: Depending on the snack selected, different helper text is provided for the quantity input box (beverages and non-packaged food trigger a helper message). 

**Quantity input**: Since the quantity attribute is what provides numerical data on the Your Snacks and Ridgeline Snacks page, the quantity input box does not allow anything other than mathematical inputs. This was implemented by typing the input to "number," but this included "e", "+", and "-". As those characters would cause problems for the numerical analysis on the Your Snacks and Ridgeline Snacks page, a further validation was implemented.

**Add Snack button**: This button is not active unless all of the fields have values and the quantity field contains only numerical values. 

### Your Snacks
**Donut chart**: The entries each user inputs feed into data for a donut chart. The key indicates the actual number of each snack consumed. Hovering over either the snack name in the key or a segment in the donut shows what percentage of total snacks that snack represents. 
