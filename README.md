# COSC310

The GUI with interface with history of conversation was already made for the A2 submission

  In the original chatbot, the bot was a sales representitive of adidas selling shoes. For this assignment I have added the function to buy socks as well. If the user does not specify what to buy, the bot will ask if they want to buy shoes or socks and then proceed to provide details of the products that the user specified.
[23:40:45] You: hello
[23:40:46] Bot: Hello sir/madam, how are you doing today?
[23:40:56] You: I would like to buy some products
[23:40:56] Bot: Would you like to purchase some shoes or socks?
[23:41:04] You: shoes
[23:41:04] Bot: What type are you looking for?

  In the original, if an unknown phrase was entered, the bot would just say that it doesn't understand and then ask the user to re-enter something else. I have added more phrases to give a certain reply at certain stages of the chat. For example if the bot asks the user for a confirmation for buying a specific shoe and the user enters something invalid, the bot will say it doesn't understand and ask for the confirmation again(with details of the same shoe). After checkout, the bot will ask if the user wants to buy more products, this also has a different response if the user inputs something invalid. If the user inputs a something invalid at a non-specific stage that doesn't require confirmation, the bot will randomly choose one of a few replies which tells the user that it does not understand and gives a suggestion of a phrase that the user can input.
[23:43:34] You: hello
[23:43:34] Bot: Hello sir/madam, how are you doing today?
[23:43:38] You: what
[23:43:38] Bot: I'm not sure what you meant. Try "I want to buy running shoes"
[23:43:51] You: I would like to buy running shoes
[23:43:53] Bot: Here are the running shoes that we have: 

1) Product: Alphaedge 4D Shoes, Price: 450
URL: https://www.adidas.ca/en/alphaedge-4d-shoes/CG5526.html
2) Product: adidas x Game of Thrones Night's Watch Ultraboost Shoes, Price: 250
URL: https://www.adidas.ca/en/adidas-x-game-of-thrones-nights-watch-ultraboost-shoes/EE3707.html
3) Product: adidas x Game of Thrones House Lannister Ultraboost Shoes, Price: 250
URL: https://www.adidas.ca/en/adidas-x-game-of-thrones-house-lannister-ultraboost-shoes/EE3710.html
4) Product: Ultraboost Shoes, Price: 250
URL: https://www.adidas.ca/en/ultraboost-shoes/BB6149.html
 Please type the shoe number that you want to purchase.
 
[23:44:01] You: 2
[23:44:01] Bot: Alright, selected adidas x Game of Thrones Night's Watch Ultraboost Shoes for $250. Would you like to checkout?
[23:44:07] You: what
[23:44:08] Bot: Sorry I didn't understand your response. Would you like to continue to checkout with adidas x Game of Thrones Night's Watch Ultraboost Shoes
[23:44:13] You: yes
[23:44:13] Bot: Successfully checked out your product: adidas x Game of Thrones Night's Watch Ultraboost Shoes.
Would you like to purchase another one?
[23:44:16] You: what
[23:44:16] Bot: Sorry I didn't understand your response. Please try again!
[23:44:31] You: yes
[23:44:31] Bot: What type are you looking for?

  I added a spellcheck using a library called jazzy. How it works is that the user inputs a message and then that string is broken down into individual words and stored in a string array. Each word in the string array is then inputed into the spellchecker which returns a suggested word based on the mispelled word and the mispelled word will be replaced by the suggested word and if the word is not mispelled the spellchecker does not return anything. After going throught the whole array, it is put back together into one string again and continues to the next part of the program as usual.
[23:41:59] You: helol
[23:42:00] Bot: Hello sir/madam, how are you doing today?
[23:42:11] You: I am doign welel
[23:42:11] Bot: Great, how may I help you today?
[23:42:27] You: I wolud liek to byu soem shose
[23:42:28] Bot: What type are you looking for?
