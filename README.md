## MERN Setup

#### Version Control and Dependencies

1. Create repo
2. `npm init`
3. Create `.gitignore`
4. Install dev dependencies:
   - nodemon
5. Install dependencies:
   - bcryptjs
   - body-parser
   - concurrently
   - express
   - lodash.isempty
   - jsonwebtoken
   - mongoose
   - node-sass
   - passport
   - passport-jwt
   - validator
6. Update scripts in `package.json`
   - `"start": node server.js`
   - `"server": "nodemon server.js"`
   - `"client": "npm start --prefix client"`
   - `"dev": "concurrently \"npm run server\" \"npm run client\""`

#### Backend

1. Set up MongoDB Atlas; get mongoURI
2. Create `config` dir with a `keys.js` for `mongoURI` and jwt `secretOrKey`
3. Create `server.js`
   - require dependencies
   - require routes
   - instantiate app
   - bodyparser middleware
   - db config and connection
   - passport middleware and config
   - Use routes
   - app.listen to port
4. DB schema setup
   - `models` folder and `User.js`
   - instantiate schema (`new mongoose.Schema`)
5. Set up form validation for registration/login
   - `validation` folder and `register.js`
   - `login.js` validations when ready
6. Set up routes
   - `routes` folder and `users.js` routes
   - require dependencies
   - load input validations for register and login
   - load user model
   - describe POST route for new user
   - describe POST route for login
7. Create `passport.js` in `config`
   - require applicable strategy
   - require `User` model and key
   - `passport.use()`
