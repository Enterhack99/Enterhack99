Nebo-clone - Render-ready repository

Instructions:
1) Push this repository to GitHub.
2) On Render create a new Web Service and connect the repo.
   - Build command: npm install
   - Start command: npm start
3) Set environment variables on Render (recommended):
   - ADMIN_USER (optional)
   - ADMIN_PASS (optional)
   - JWT_SECRET (recommended)

The postinstall script builds the React client so the server will serve static files from client/build.
Admin default: admin / ChangeMe123!
