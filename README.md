# MERN Blog — Server

REST API for a full-stack blogging platform, built with Node.js, Express and MongoDB.

**Front end:** [MERN-blog-app-client](https://github.com/yassine-ouerfelli/MERN-blog-app-client)

## Features
- User registration with password hashing (bcrypt) and input validation
- JWT authentication with logout and "log out of all devices"
- Google sign-in (google-auth-library)
- Email confirmation and password reset via Nodemailer
- Blog posts: create, list, read, edit
- Favourites per user

## Main endpoints
| Method | Route | Description |
|---|---|---|
| POST | `/register` | Create an account |
| POST | `/login` | Log in, returns a JWT |
| POST | `/api/googlelogin` | Log in with Google |
| POST | `/forget` | Send a password-reset email |
| GET | `/users/me` | Current user (auth) |
| POST | `/addblog` | Create a post (auth) |
| GET | `/` | List all posts |
| GET | `/blog/:id` | Get one post |
| GET | `/favblog` | Current user's favourites (auth) |

## Tech stack
Node.js · Express · MongoDB · Mongoose · JWT · bcrypt · Nodemailer

## Getting started
```bash
git clone https://github.com/yassine-ouerfelli/MERN-blog-app-server.git
cd MERN-blog-app-server
npm install
```
You need a local MongoDB instance (`mongodb://127.0.0.1/blog-project`) and a `.env` file:
```
GOOGLE_ID=your-google-client-id
GMAIL_ADRESS=your-gmail-address
GMAIL_PASSWORD=your-gmail-app-password
```
Then run:
```bash
npm start
```
