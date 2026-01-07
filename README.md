# AI Clauset

Welcome to AI clauset, your personal helper to select your day to day outfits. This is an AI-based solution to create day to day outfits. There is no longer a need to spend hours next to the wardrobe. AI Clauset will create outfits based on current weather conditions and the clothes' images that user has uploaded.

<p align="center">
  <img height="500" alt="ai-clauset" src="https://github.com/user-attachments/assets/07fe5176-1a14-426f-9562-f52c0d1989f4" />
</p>

We invite you to complete a little walkthrough below to see the key features of our application. It will show what our application is currently capable of as well as how it utilizes AI in its work.

<br>

## Walkthrough

- [Account Creation](#account-creation)
- [Adding Clothes (AI used)](#adding-clothes-AI-used)
- [Generate Outfit](#generate-outfit)
- [Weather Setup (AI used)](#weather-setup-AI-used)

<br>

# Account Creation

Let's start our journey with signup. On the Home page on the top left corner click SignUp button.
<img width="1891" height="902" alt="image" src="https://github.com/user-attachments/assets/77522f02-09ee-47f9-806a-7c8013a89e8c" />

On the appeared form you are asked for "your name", "email" and "password". Fill out those fields with corresponding information and click "Create my account".

Mock examples of information that you can input:

- "Your name": "Alex"
- "Email": "alex@email.com"
- "Password": "12345"

After you have created account, you should see the main page of the application with your name on top.
<img width="1885" height="908" alt="image" src="https://github.com/user-attachments/assets/c13d49b2-d98c-40e3-81af-351f18cef8b6" />

<br><br><br>

# Adding Clothes (AI used)

You won't see any outfits on the Home page as you don't have any clothes. Let's add some.
You have an option to click "+" button in the bottom right corner on the home page OR go to "My Wardrobe" in the navbar and click "Add New Cloth" button at the bottom of the page.

Option 1 (Click "+" button):
<img width="1885" height="908" alt="image" src="https://github.com/user-attachments/assets/c81da702-6559-4b31-9c53-bb281a9a25a3" />

Option 2 (Click "Add New Cloth" button):
<img width="1886" height="900" alt="image" src="https://github.com/user-attachments/assets/e3c486a4-4db7-412a-a75a-f95d85370882" />

In any case you will be presented with a modal asking you to enter cloth information.
All fields are required and you are asked to upload a cloth image, enter its name, enter an occasion for which you feel comfortable wearing this cloth and enter a temperature under which you feel comfortable wearing this cloth.

**AI USED:** You can witness the use of AI when you appload an image of an item.
After a small amount of time as you upload an image of a cloth, you will see that cloth type was identified. Note: auto detection only works for .png and .jpg images.
<br>
<img height="390" alt="image" src="https://github.com/user-attachments/assets/847f23ce-a67a-4996-a29f-407b6d58b5cc" />

The way we get this AI prediction:

- Step 1: Grab url of the uploaded image (once image is automatically uploaded to UploadCare service, so we grab this image's url that service).
- Step 2: Send URL to the prediction model. AI Model was trained to identify the type of cloth from the image.

  <img height="390" alt="image" src="https://github.com/user-attachments/assets/00a7c046-b41f-4832-9f20-e6e9539076fa" />


- Step 3: Process the output object from the prediction model and set UI form input with get the tag name that has the highest probability.
  <img width="1526" height="641" alt="image" src="https://github.com/user-attachments/assets/0a797fa9-100a-455e-b32c-994cfae5bcc1" />

If you need, you can find clothes mock information in "[Clothes Mock Information](#clothes-mock-information)" section at the bottom for a quick application test.
Fill out the rest of the information for the cloth and you will see that cloth has been added to your virtual wardrobe.

<br>
<img height="390" alt="image" src="https://github.com/user-attachments/assets/9aa3332b-c1c6-4a12-85fc-5efc22f90a65" />

<br><br>

# Generate Outfit

Great, you have 1 cloth added to your virtual wardrobe. That's a good start. An outfit requires to have 2 clothes (TOP and BOTTOM) for the same occassion. Therefore, let's add another cloth for the same occasion, so that we can see the first outfit.
<br>
<img height="350" alt="image" src="https://github.com/user-attachments/assets/43bee2dd-b751-446b-a544-efc19bb97ffc" />
<img height="350" alt="image" src="https://github.com/user-attachments/assets/a76ba6d4-9387-4919-9fc2-5f65892f251f" />

Now, return to the home page. You can now see that we have a generated outfit for the occasion for which we have met the requirement of adding at least 1 top and 1 bottom cloth.
<br>
<img height="390" alt="image" src="https://github.com/user-attachments/assets/b9f62e9e-274f-47f5-bbe5-dbcde05a585f" />

You are absolutely free to add multiple clothes (tops and bottoms) for the same occassion. Whenever you click "Re-Generate Outfits" button in the bottom left corner of the home page, application will select 1 top and 1 bottom out of the pool of clothes for the same occasion.

For instance, let's add another bottom item for the casual occasion.
<br>
<img height="350" alt="image" src="https://github.com/user-attachments/assets/f031563d-a0a9-4256-9575-bd210df54c5f" />
<br>
Now, there are 3 clothes in the virtual wardrobe.
<br>
<img height="350" alt="image" src="https://github.com/user-attachments/assets/099f53a4-0aad-4941-9b3a-999aca5a73cb" />
<br>
Now, whenever you click "Re-Generate Outfits" on the home page, Casual outfit might change and show you another bottom. The more clothes you have for the same occasion, the more likely the outfit will change for that occasion whenever you click "Re-Generate Outfits".
<img width="1883" height="902" alt="image" src="https://github.com/user-attachments/assets/44a1989c-d1b7-400e-95c5-46ff495b66ae" />
<img width="1886" height="894" alt="image" src="https://github.com/user-attachments/assets/b59017b5-7deb-48ac-8c8b-86328c84d81c" />

Let's continue and add clothes, so that we have another outfit for Formal occasion.
<br>
<img height="350" alt="image" src="https://github.com/user-attachments/assets/cb98436b-a835-4b5c-9483-aa3727ac29f1" />
<img height="350" alt="image" src="https://github.com/user-attachments/assets/961f72c3-d3b1-459d-bf3c-5047469ff3b9" />

Our virtual wardrobe is getting larger!
<img width="1888" height="900" alt="image" src="https://github.com/user-attachments/assets/68fcff49-7b89-4abf-8679-51dfc54dca46" />

Now, go back to the Home page, where you can now witness another outfit for "Formal" occasion.
<img width="1883" height="899" alt="image" src="https://github.com/user-attachments/assets/1333fc4b-4012-4a05-ac33-f1627096a73c" />

<br><br>

# Weather Setup (AI used)

Our application can help you make sure that your outfits match current weather conditions. All you have to do is enable your location and application will do everything for you!
<br>
Go to the "My Account" page using navbar and click on "Detect" next to Location.
<img width="1915" height="897" alt="image" src="https://github.com/user-attachments/assets/a7916dba-e5f5-4a8b-a45c-2b6834683637" />

You might be prompted to allow your location. Click "Allow" if you want to have outfits matched depending on current weater conditions.
<img height="150" alt="image" src="https://github.com/user-attachments/assets/b4030457-74f7-46c5-b2fd-7ebe13f3dbd1" />

After you allow your location, you will see that location input was automatically filled. Enter your current password to confirm the changes and click "Update Account" button.
<br>
<img height="350" alt="image" src="https://github.com/user-attachments/assets/67b37984-1b15-4390-8f47-74dbe77e6038" />

After you update account with your location, you can return back to the home page, where you can witness current weather conditions in your location on the right side.
<br>
**AI USED:** You can witness the use of AI as it suggest you what you can think of wearing considering your weather conditions (weather, humidity, wind, etc).
<img width="1888" height="901" alt="image" src="https://github.com/user-attachments/assets/25ad5e53-ddae-4fdf-8d89-fb6ed9a63111" />

There are a few steps to get this AI suggestion:

- Step 1: Extract weather information received from Open Weather API
- Step 2: Make a fetch to the AI model with the current weather conditions
  <img height="500" alt="image" src="https://github.com/user-attachments/assets/2cfc05ce-bece-4d04-9bff-b5b79e9ed674" />
  
  AI Model was trained with a set of different columns describing the weather to make decisions on the clothes suggestions based on the received weather conditions in your city.
  
  <img height="390" alt="image" src="https://github.com/user-attachments/assets/6175c591-b09a-4258-9de2-e0b3baf0e339" />


Also, note that outfits do not have clothes, which temperature is outside too far from the current temperature (for over 10 degrees). In our case, current weather temperature is 12 degrees, so there are not clothes outside of range ~[2 degrees, 22 degrees].
<br>
Let's test that can test that. If we ecit all clothes for Casual occasion to have temperature below 0, we should not be shown Casual outfit at all (since all clothes don't match current weather conditions).
<img width="1883" height="900" alt="image" src="https://github.com/user-attachments/assets/bd412227-a913-4466-a1d2-259e76debbad" />
As discussed, we cannot see Casual outfit anymore as neigher of casual clothes match current weather conditions.
<img width="1885" height="896" alt="image" src="https://github.com/user-attachments/assets/227af5a1-c9d6-487a-8991-54e527a7a40c" />


AI model is the backbone of this application. To summarize what was explained above, the training was performed using the total of 9 columns: 2 categorical representing clothing types for the upper and lower body & 7 numerical describing different weather conditions.

<img height="390" alt="image" src="https://github.com/user-attachments/assets/65601e0f-2477-4407-b43a-6d826c622acd" />


# Clothes Mock Information

### Casual

|             | Cloth 1                                                                                                                                   | Cloth 2                                                                                                                                   | Cloth 3 (optional)                                                                                                                        |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Image       | <img height="200" alt="image" src="https://github.com/user-attachments/assets/2324e28f-e400-4e91-8e5a-9f193128cfa0" /> | <img height="200" alt="image" src="https://github.com/user-attachments/assets/560a8baf-10fe-474c-9217-4c244178c37c" /> | <img height="200" alt="image" src="https://github.com/user-attachments/assets/71680adf-2082-4b67-a549-42cc6e9fe01b" /> |
| Name        | Warm Trousers                                                                                                                             | Parka                                                                                                                                     | Jeans                                                                                                                                     |
| Type        | Bottom                                                                                                                                    | Top                                                                                                                                       | Bottom                                                                                                                                    |
| Occasion    | Casual                                                                                                                                    | Casual                                                                                                                                    | Casual                                                                                                                                    |
| Temperature | -15                                                                                                                                       | -5                                                                                                                                        | 5                                                                                                                                         |

### Formal

|             | Cloth 1                                                                                                                                   | Cloth 2                                                                                                                                   |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Image       | <img height="200" alt="image" src="https://github.com/user-attachments/assets/35db3c26-a2c6-4341-a82a-215571fbb6f8" /> | <img height="200" alt="image" src="https://github.com/user-attachments/assets/28cf88b5-9815-4960-a94a-3493d7aea21f" /> |
| Name        | Pants                                                                                                                                     | Shirt                                                                                                                                     |
| Type        | Bottom                                                                                                                                    | Top                                                                                                                                       |
| Occasion    | Formal                                                                                                                                    | Formal                                                                                                                                    |
| Temperature | 10                                                                                                                                        | 12                                                                                                                                        |

### Sporty

|             | Cloth 1                                                                                                                                   | Cloth 2                                                                                                                                   |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Image       | <img height="200" alt="image" src="https://github.com/user-attachments/assets/a322c845-5533-42e1-8ec6-b9d448f93c9d" /> | <img height="200" alt="image" src="https://github.com/user-attachments/assets/5a1d5805-fe08-4aee-b4db-633e9cc68593" /> |
| Name        | Shorts                                                                                                                                    | T-Shirt                                                                                                                                   |
| Type        | Bottom                                                                                                                                    | Top                                                                                                                                       |
| Occasion    | Sports                                                                                                                                    | Sports                                                                                                                                    |
| Temperature | 25                                                                                                                                        | 20                                                                                                                                        |
