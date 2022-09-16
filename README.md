# Examination in CMS


## Getting started

For this project you need to have a WordPress.com website. 

### Built With

This project is built with 

![Vue](vuejs.jpg)


### Installation
Depending on if you want to deploy on your own you need to fork this repository, if not then you can just clone it.

1. Clone this repository to start with.
   ```bash
   git clone https://github.com/IzaMarkstrom/wordpress-frontend-vue.git
   ```
2. Install NPM packages
   ```bash
   npm install
   ```
3. Create a .env file with your API URL with this variable name
   ```bash
   VUE_APP_BACKEND_URL = "ENTER YOUR URL"
   ```

4. To create new posts to the WordPress backend, send your username or email address to:

   * markstrom93@hotmail.com

## Run 
To start this project you write this in the terminal
   ```bash
   npm run serve
   ```
Which opens at port 8080

![localhost](localhost.jpg)

## Deploy
This project is deployed in Vercel [here](https://wordpress-frontend-vue.vercel.app/)

Vercel won't deploy your code unless you push to GitHub. So you can test your code using the localhost before pushing to GitHub.

## Deploy on your own
You need to have forked the project for this step.

1. Go to [Vercel](https://vercel.com/dashboard) and create an account/ log in.
2. Add new - project
3. Connect GitHub to Vercel 
4. Import your repository
5. Add environmental variables (same as in your .env file)



## Contact
Administrator: Iza Markström

Github: [IzaMarkstrom](https://github.com/IzaMarkstrom)