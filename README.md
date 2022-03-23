# **Test project**

A test project to test out all common git commands

## Commands used:

### Initializing a local git repo

## 1. Configure Git settings in your local machine
```html 
git config global user.name <your name>
git config global user.email <your email>
```

## 2. Initialize Git in any of your local repo
```html
git init 
```

## 3. At first only master branch is created, so add/stage all files inside the local folder with the following command first

### to add a single file 
```html 
git add <file-name>
```

### to add all files
```html 
git add .
```

### to unstage all file
```html 
git reset
```

### OR unstage any single file
```html 
git reset <file-name> OR git restore --staged <file>
```

## 4. Commit all the staged file in the master branch
```html 
git commit -m "your message" <any single file name> or keep blank for commtting all staged file at once
```

## 5. Now to check the status of the working tree type,
```html 
git status 
```





