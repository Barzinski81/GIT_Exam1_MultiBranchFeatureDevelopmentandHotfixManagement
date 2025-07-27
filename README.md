```
mkdir multi-branch
cd multi-branch/
git init

echo "Initial content" > index.html
git add .
git commit -m "Initial content"

git checkout -b feature-auth
echo "console.log('Auth feature');" > auth.js
git add auth.js
git commit -m "Added initial authorization feature"
echo "console.log('Login funtionality');" >> auth.js
git add auth.js

git commit -m "Added Login to the authorization feature"
echo "console.log('Registration feature');" > register.js
git add register.js
git commit -m "Added registration form"
echo "console.log('Password recovery feature');" >> register.js
git add register.js
git commit -m "Added password recovery feature"

git checkout main
git checkout -b feature-dashboard
echo "Dashboard User Interface" > dashboard.html
git add dashboard.html
git commit -m "Added basic Dashboard UI"
echo "Advanced Dashboard features" >> dashboard.html
git add dashboard.html
git commit -m "Added advanced Dashboard features"

echo "Intial widget funtionality" > widgets.js
git add widgets.js
git commit -m "Added initial widget functionality"
echo "Additional widget functionalities" >> widgets.js
git add widgets.js
git commit -m "Updated widget functionality"

git checkout main
```

<img width="654" height="243" alt="image" src="https://github.com/user-attachments/assets/6b1fccba-43ed-44f1-8d87-cadba5ff439e" />

```
echo "Critical security bug" >> index.html

$ cat index.html
Initial content
Critical security bug

git add index.html
git commit -m "Introduced security bug"

git checkout -b hotfix-security
sed -i 's/Critical security bug/Bug fixed/' index.html

$ cat index.html
Initial content
Bug fixed

git add index.html
git commit -m "The security bug was fixed"

git checkout main

$ git status
On branch main
nothing to commit, working tree clean
```

<img width="683" height="318" alt="image" src="https://github.com/user-attachments/assets/6975d277-fe77-43ca-9a10-de28c44455fd" />

```
git merge hotfix-security

Merge made by the 'ort' strategy.
 dashboard.html | 2 ++
 widgets.js     | 2 ++
 2 files changed, 4 insertions(+)
 create mode 100644 dashboard.html
 create mode 100644 widgets.js

git merge feature-auth
```

<img width="418" height="146" alt="image" src="https://github.com/user-attachments/assets/ebccbdc5-e447-4b54-8930-fba3c457761e" />

```
git merge feature-dashboard
```

<img width="393" height="136" alt="image" src="https://github.com/user-attachments/assets/f449585d-d8d5-4149-9889-18a24e1fc198" />

```
git reflog before intercative rebase:
```

<img width="879" height="484" alt="image" src="https://github.com/user-attachments/assets/5d2de347-ddf8-4727-ac88-6df8ab43c9df" />

<img width="878" height="276" alt="image" src="https://github.com/user-attachments/assets/6aae27cb-7e51-47e6-b145-7275403b6827" />

<img width="676" height="236" alt="image" src="https://github.com/user-attachments/assets/09ba7fdc-2fa9-4619-8864-36238af299f7" />

<img width="698" height="364" alt="image" src="https://github.com/user-attachments/assets/a7f9398a-1122-4db9-8c97-db5673ccc807" />

```
git log --oneline
```
<img width="607" height="170" alt="image" src="https://github.com/user-attachments/assets/317d5537-bb01-47b6-8bd4-16a7cf79d632" />

