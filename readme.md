 
# GitFlow Tutorial

### Uso Básico 
This is a repository to teach how to use gitflow

---
# Comandos 
First Start the repository by giving this command: 

```
git flow init
```

He will give you successive messages like this one, suggesting names (you can change them and put any you prefer, but the ones he segers are defaults, so I recommend using only what he suggests and not changing anything):

```
Initialized empty Git repository in /home/your_username/your_dir/.git/
No branches exist yet. Base branches must be created now.
Branch name for production releases: [master]
```

If you accept everything he suggests, just hit enter until he runs out of suggestions ;)

After that, if you give a git branch in the terminal you can see that there are two branches created, which are the main ones and will never be deleted, develop and master.

Every time we make a new feature for our application, we will always create a new feature branch within the development branch with the name of the feature in question, for example: 
```
git flow feature start feature_name 
```

in this case, if I were to make a feature for a calculator and start developing the sum function, it would look like this:

```
git flow feature start sum
```

In this case, for educational purposes, I will create a text file, called sum, like this:
```
touch sum
```

## explanation

Just for the sake of understanding, " touch " is a command we use in the Linux/MacOS terminal to create any type of file.

## Comandos
Now that I've created the file and in theory added all the code and it's working as it should, I'm going to add this file to git, using this command:
```
git add .
```

Just for the sake of explanation, the "git add ." is used to add new and modified files but not delete ones.


Right after giving the command git add ., give this command right after:

```
git commit -m 'Adiciona funcionalidade Soma'
```


It's all over, it's committed, all the functionalities of that part of the project/calculator are ready, Matheus, now what?

### Now issue this command:
```
git flow feature finish feature_name
```

for example, I was doing the sum functionality, it would be like this:
```
git flow feature finish sum
```

After that, you will release the two features that went to development in release, using this command:
```
git flow release start 0.1.0
```
In case, after start, you put the release version number you are doing, then you put it according to what your company proposes, it could be:
```
git flow release start 1.1.0
or
git flow release start 1.0.0
or
git flow release start 2.0.1
etc
```

Now you can close your release if the QA has already seen it and passed it by the customer, using:
```
git flow release finish release_number
```

for example:
```
git flow release finish 0.1.0
```











