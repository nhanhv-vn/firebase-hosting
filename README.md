# Step by step to deploy static site with Firebase hosting

## Author:

- Nhan Huynh

- Email: nhanhv.pnv@gmail.com

- Phone: +84 355978217

- Github: https://github.com/nhanhv-vn/

## Introduction

### Firebase hosting
   - Provides hosting for your web app, static and dynamic content and microservices

       - More detail: [Link](https://firebase.google.com/docs/hosting)

- Why choose Firebase hosting to deploy

    - Easy to configuration

    - Fast content Delivery

    - Easy to Rollback version

    - Easy to customize domain & SSL

    - One more important with me: *FREE 1GB store SSD*. Of course, it is very easy to expand more storage

- Basic step by step deploy static

    - Have a gmail account

    - Access to Firebase console, choose a *name* and add a project

    - Install the Firebase CLI(npm install -g firebase-tools)

    - Set up a project directory(cd your_folder - firebase login - firebase init)

    - Deploy project to hosting(firebase deploy)

    - Add your domain if you have one

### Basic config

- *.firebaserc*: Config app project name(Project container hosting) will be deploy to host

- *fire.json*: Config soure code will upload to host and config URLs

### Testing config on local first

- Run `firebase serve`

- Open your browser and run at `http://localhost:5000/`

### Deploy

- Run `firebase depploy`

- Get domain return after deployed from firebase cli and run your site.

- Demo: https://landing-page-58c92.web.app/


### Custom domain 

- Step 1: Enter the custom domain that you'd like to connect to your Hosting site

![Step_1](https://github.com/nhanhv-vn/firebase-hosting/blob/develop/Step_1.png)


- Step 2: Verify your domain ownership with you DNS records

![Step_2](https://github.com/nhanhv-vn/firebase-hosting/blob/develop/Step_2.png)

### Notes

- Template static files download from https://html5up.net/

## Advance

- Auto deploy static page with github + travis ci

### Prepare

- [Github](https://github.com/) account/repository to push source code
- 
- [Travis](https://docs.travis-ci.com/) account and Sync account with github account

### Setup auto deploy
- Create .travis.yml

- Setup environment variables on travis [Docs](https://docs.travis-ci.com/)

- Writing script deployment

- Push code to github and reward yourself with a beer

## Notes

- Get firebase token
Run `firebase login:ci`

- Add more *Makefile* to add more tasks before run deploy
