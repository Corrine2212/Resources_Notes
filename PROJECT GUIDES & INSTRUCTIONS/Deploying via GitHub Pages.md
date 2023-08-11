## Deploying simple HTML, CSS & JS Projects

1. Create Github repo
2. `git init` your project
3. `git add .` and `commit -m ''`
4. git push to Github repo that you set up
5. Go to settings, look for 'Pages'
6. Under 'Branch' select 'main' branch
7. Click 'Save'
8. Give it a few minutes for your page to deploy


## Deploying React JS Projects

**Step 1: Create your GitHub repo**   
- Make sure to take note of your GitHub username   

**Step 2: Create your React app**
- cd into the directory you want to work in. In terminal run the following command;
	```bash
	npx create-react-app portfolio
	```
   
**Step 3: Install Github Pages as a Dev-Dependency**
- Install gh-pages by cd-ing into your React app and running:
	```bash
	npm install gh-pages --save-dev
	```
- This package will create a branch on GitHub called 'gh-pages'
- This branch is just for deployment

**Step 4: Update your package.json file**    
- Add a homepage
	```json
	"homepage": "https://<username>.github.io/<repo-name>" 
	```

- Add a predeploy
	- In the scripts section, add a predeploy:
```json
	"predeploy": "npm run build"
```

- Add Deploy
	- Also in the scripts section, add a deploy:
```json
	"deploy": "gh-pages -d build"
```

**Step 5: Push to Github**
- Once you've completed the above steps, push your changes to GitHub. Run the following commands:
```bash
git add .

git commit -m "first commit"

git branch -M main

git remote add origin <repository URL>

git push -u origin main
```

**Step 6: Deploy**
- run the following command
```bash
npm run deploy
```

**Step 7: Update your repo settings**
- Go to settings in your repo and look for Pages section. 
- Underneath the Source heading, you should have option to select which branch the site is being built from. If it isn't already change the branch to `gh-pages`. 

**Future updates**
- Every time you update your app (make sure you're on  main branch) 
- Run `npm run deploy` to update your site. This will take a few minutes to update.