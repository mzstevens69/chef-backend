# Chef Portfolio team

## Endpoints




                                 
   # Register New User
   
  ### EndPoint :




| Method        | EndPoint           | 
| ------------- |:-------------:| 
| POST      | api/auth/register|



                        
                                                              
  ### New User Object: 
   
   
   
   
   | field        | metadata           | 
   | -------------|:-------------:| 
   |   firstname    |  Required   |
   |   lastname    |  Required   |
   |  username   | Required and Unique
   |   password    |  Required   |
   |    email       |  Required and Unique |
   |   phone       |  Optional and Unique  |
   |      state       |  Optional  |
   |     city        |  Optional   |
   |    address     |  Optional    |
   |    zipcode     |  Optional    |

                    
   
   
   
 
            

   # Login User
   
  ### Users for Test: 
   
   
   
   | username        | password           | 
   | -------------|:-------------:| 
   | test1     |     test1  | 
   | test2     |     test2   |
   | test3     |     test3   |
   
   
   
   
   
  ### EndPoint
   
   
   Method        |           EndPoint
   | -------------|:-------------:| 
   | POST         |  api/auth/login|
                   
                       
   
  ### Login User Object: 
   
   
   
   | field        | metadata           | 
   | -------------|:-------------:| 
   | username     |     Required  | 
   | password     |     Required   |
   
   
   
   
   
   # Global Recipes
   
  * To Show all the recipes of the users without login.
   
   Method        |           EndPoint
   | -------------|:-------------:| 
   | GET         |  api/recipes|
   
   
   
   * To Show the recipe By Id without login.
   
   
   Method        |           EndPoint
 | -------------|:-------------:| 
 | GET         |  api/recipes/:id|
                   
   
   
 # APIs with authorization:
 
 ### must LogIn and have a token to make these requests:
 
 
 * make a request with the id of the user to get all the recipes of the user and add new recipe.
 
 
  Method        |       EndPoint | Description
 | -------------|:-------------:| ----------|
 | GET         |  api/auth/user/:id|  get all recipes
  | POST         |  api/auth/user/:id|  add new recipe
  
  
  
  ### Recipe Object:
  
  
  | field        | metadata           | 
   | -------------|:-------------:| 
   |  recipe_name   | Required 
   |    mealtype       |  Required  |
   |   ingredients    |  Required   |
   |    instructions       |  Required  |
   
   #### Mealtype :
   
   the Mealtype of the recipe object should be one of these values :
   
   | field        | value           | 
   | -------------|:-------------:| 
   | breakfast   | 1 
   |    lunch      |  2  |
   |   dinner    |  3   |
   |    snack       |  4  |
   |    dessert       |  5  |



 
## Update/Delete Recipe
 * make a request with the id of the recipe to update or delete recipe.
 
 
 
 Method        |       EndPoint | Description
 | -------------|:-------------:| ----------|
 | PUT         |  api/auth/user/recipes/:id|  Update recipe
  | DELETE         |  api/auth/user/recipes/:id|   Delete recipe




### BackEnd Build with Node.js
   ### Libraries:
   * express
   * knex
   * bcryptjs
   * jsonwebtoken
