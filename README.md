# Taxi-opproximation-for-redmerble.ai

## Project description: 

You are an event planner for a small Melbourne consulting firm. Your organization is holding an event in the Gold Coast which requires everyone to fly from Melbourne’s Tullamarine airport at Departure Dr, Melbourne Airport, VIC 3045. Your company has decided to organize taxis for its employees, but wants to minimize the total cost paid (ie total distance travelled while carrying at least one passenger) by having employees share taxis where possible.!


## Assumptions:
- The address that they provide are all valid. no missing or wrong values
- There are outlier but we are keeping them since all the values are necessary for us to work with
- The employees are good friends with each other, they are comfortable with sharing one taxi
- There is a trade off between time of arriving and cost of the taxi

## Data pre-processing:
- dont really need to data cleaning, since we assumed the data provided are valid
- we get the latitude and longtitute of each address for further application, put them in the data frame as new attributes

## Approach to this problem:

- I put as many people as we can into one taxi(which is 4) to save the money on calling extra taxis.
- There are 75 employees. We call 19 cabs for them. 18 of them have 4 people in it, 1 one them have only 3 people
- we make sure that the time of picking up wont take too long, so I chose 4 closest people to get into one taxi (using k-means) 
- In each cluster, we pick up the one has got longest distance from the airport first, then go to the second, second last then the last. (it's pretty naive). we can use google map api later on to improve it.
- or we can let employees go to the pick up location by themselves the pick up location can be the centre of the cluster (this way can save so much time pick up time and also cost of taxis),it's just an option
- find the fee of each employee have their own taxi and the fee of a taxi takes 4 employees, also the difference between them

## future steps:
- look deep into trade off between cost and time
- use google map api to check the duration between each address and airport
- expand the project further for larger data sets 

## output maps && plots
<img width="974" alt="Screen Shot 2021-08-10 at 3 42 38 pm" src="https://user-images.githubusercontent.com/37463240/128814787-4f850d94-56a9-4115-9549-78a0b0e7ba7d.png">
<img width="1020" alt="Screen Shot 2021-08-10 at 3 42 53 pm" src="https://user-images.githubusercontent.com/37463240/128814804-0fa7a9b3-a3a7-4695-a081-2da3a81a8e41.png">
<img width="1307" alt="Screen Shot 2021-08-10 at 3 47 22 pm" src="https://user-images.githubusercontent.com/37463240/128814814-2a08b7e0-ec0f-45a7-8873-32c7bb71d04b.png">
https://user-images.githubusercontent.com/37463240/128814924-fee75a80-0071-404e-8123-5debfb893eea.png



