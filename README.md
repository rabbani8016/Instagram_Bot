# Instagram_Bot
Instagram Bot using Instagrapi

This is a Python-based Instagram automation bot that can perform various tasks such as fetching followers, uploading images, liking posts, and more using the instagrapi library.

# Features
Login to Instagram using credentials.
Fetch Followers of a user.
Upload an Image with a caption.
Like Posts and Comment on them.
Follow and Unfollow Users.
Send Direct Messages (DMs).

# Installation

1. Clone the Repository

git clone https://github.com/yourusername/InstagramBot.git
cd InstagramBot

2. Create and Activate a Virtual Environment

python -m venv InstagramBotEnv

For Windows:

InstagramBotEnv\Scripts\activate

For Mac/Linux:

source InstagramBotEnv/bin/activate

3. Install Dependencies
pip install instagrapi

# Usage
1. Run the Script to Fetch Followers

from instagrapi import Client

bot = Client()
bot.login("your_username", "your_password")

# Get followers of a user
user_id = bot.user_id_from_username("your_username")
followers = bot.user_followers(user_id)

for follower_id, follower_info in followers.items():
    print(f"{follower_info.username} - {follower_info.full_name}")

2. Upload an Image

bot.photo_upload("image.jpg", "This is a test upload!")

3. Like a Post

media_id = bot.media_pk_from_url("https://www.instagram.com/p/POST_ID/")
bot.media_like(media_id)

4. Comment on a Post
bot.media_comment(media_id, "Nice post!")



# Notes:
1.Avoid excessive automation to prevent being blocked by Instagram.
2.Use proxies if you're automating multiple accounts.
3.Two-Factor Authentication (2FA) must be disabled for login to work.
