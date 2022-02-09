# Reboot_Project-2-PetsAreKings
PetsAreKings, is an online application focused on connecting pet owners with loving pet-sitters. PetsAreKings allows users to search for a professional pet-sitter to come over to their homes or, instead, to leave their animals friends under the care of our pet lovers.

## API Endpoints

All API Request must be prepended with /api            


### Authentication Endpoints

METHOD | ENDPOINT         | TOKEN | DESCRIPTION              | POST PARAMS                                     | RETURNS
-------|------------------|-------|--------------------------|-------------------------------------------------|-----------------------------
POST   | /auth/signup     | -     | User Signup              | name, surname, username, email, password, role  | token
POST   | /auth/login      | -     | User Login               | email, password                                 | token
GET    | /auth/check      | YES   | Auth Token check         | -                                               |


### User Profile Endpoints

METHOD | ENDPOINT        | TOKEN | DESCRIPTION                   | POST PARAMS                                                      | RETURNS
-------|-----------------|-------|-------------------------------|------------------------------------------------------------------|--------------------------------
GET    | /user/profile   | YES   | Shows registered user profile |  -                                                               | name, surname, username, email, pets, Geolocation, avatar
PUT    | /user/profile   | YES   | Update user profile           | name, surname, username, email, pets, Geolocation, avatar, role  | updated user data
DELETE | /user/profile   | YES   | Deletes user profile          | password                                                         | confirmation of deleted user


### Cate Profile Endpoints

METHOD | ENDPOINT            | TOKEN | DESCRIPTION                   | POST PARAMS                                          | RETURNS
-------|-------------|-------|-------------------------------|--------------------------------------------------------------|--------------------------------
GET    | /user/cat/profile   | YES   | Shows registered user profile |  -                                                   | name, age, avatar, comments, star, sociable, special, picture, race
PUT    | /user/cat/profile   | YES   | Update user profile           | name, age, avatar, sociable, special, picture, race  | updated cat data
DELETE | /user/cat/profile   | YES   | Deletes user profile          | password                                             | confirmation of deleted cat


### Host Profile Endpoints

METHOD | ENDPOINT             | TOKEN | DESCRIPTION                   | POST PARAMS                                     | RETURNS
-------|----------------------|-------|-------------------------------|-------------------------------------------------|--------------------------------
GET    | /user/host/profile   | YES   | Shows registered user profile |  -                                              | username, email, address, house_type, star, picture, comments, services, pet_house_share, prices
PUT    | /user/host/profile   | YES   | Update user profile           | username, email, address, house_type, star, picture, comments, services, pet_house_share, prices  | updated user data
DELETE | /user/host/profile   | YES   | Deletes user profile          | password                                        | confirmation of deleted user


### User Endpoints

METHOD | ENDPOINT         | TOKEN | DESCRIPTION                     | PARAMS                                          | RETURNS
-------|------------------|-------|---------------------------------|-------------------------------------------------|----------------------------
GET    | /users           | YES   | Finds host by geolocation       | query: search string                            | list of matching hosts
GET    | /users/:userid   | YES   | Get user profile                | username                                        | user profile
