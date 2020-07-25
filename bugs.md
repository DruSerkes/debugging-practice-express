# Bugs

1. BUG #1: app.js exports app twice (commented out for fix)

2. BUG #2: function authUser decodes token without verifying signature with SECRET_KEY

3. BUG #3: GET /users returns personal info (email/phone)

4. BUG #4: PATCH /users allowed patching of disallowed fields - implemented API validation with JSONSchema 

5. BUG #5: PATCH /users only allowed patching by admin user - removed middleware to require admin status

6. BUG #6: GET /users/:username returning empty dataset instead of throwing 404 when user not found

7. BUG #7: POST /login doesn't await User.authenticate 