# Jäsenrekisteri-backend
Membership register backend API for Asteriski ry / Jäsenrekisterin backend API Asteriski ry:n tarpeisiin

React frontend is here <https://github.com/asteriskiry/jasenrekisteri-frontend>.

### Tech
- Node.js
- Passport.js
- Express.js
- MongoDB

### Start
Install node.js, npm and MongoDB.

Start MongoDB with `systemctl start mongodb` or `mongod`.
```bash
git clone https://github.com/asteriskiry/jasenrekisteri-backend.git
cd jasenrekisteri-backend
cp .env-sample .env
npm install
npm start
```
Configure `.env`-file if needed. You can use `npm run watch` instead of `npm start` to watch file changes with nodemon.

You can make admin account with:
```bash
npm run create-user
```

## Importing data

You can import CSV files with:
```bash
npm run import "<full-path-to-csv>" "<jasenrekisteri-token>" "<id>"
```
For example:
```bash
npm run import "/home/mjt/data.csv" "JWT 12345" "123"
```
You can get id and jasenrekisteri-token by logging in to jäsenrekisteri with admin account and checking cookies with developer tools (Application -> Cookies).

CSV data must be in this format:
```bash
firstname;lastname;utu_mail;membership_approved;membership_ends;hometown;tyy_member;tivia_member;board;
```

---
© Asteriski ry
