# RepoPusher

Hello, adventurer !

The purpose of this Github repository is very simple.

First, clone it wherever you want all your work to be. Typically, in your Desktop folder, for convenience.

```
git clone https://github.com/lanouvelleecole/RepoPusher
```

Then place all your Github repositories inside this folder.

Open the package.json file in this folder, then edit the "push-all" script like this:

```
"push-all": "cd ./Repo1Name && npm run push && cd ../Repo2Name && npm run push && cd ../Repo3Name && npm run push && cd .."
```

Replace Repo1Name and Repo2Name and Repo3Name with the names of your own repo folders you added.

If you only have 2 repos to push, then remove the ```&& cd ../Repo3Name && npm run push``` part of the script.

If you have more than 3 Repositories to push, then add as many ```&& cd ../RepoXName && npm run push``` pieces right before the very end of the script, before the ```cd ..``` end of the script.

Finally, you can use the ```npm run push-all``` script to push all your repos in 1 command.

Please note that each individual repo must have it's own "push" script in it's package.json, for this to work. You can find the "push" script right below

```
"push": "(git add . && git commit -m \"I'm a bigger pusher than Ice-T homie !!!\" && git push) || exit 0"
```

All the templates you create with ```npx maslow``` have a push script included by default !!!

That's it ! I wish you the best in your creative journey. God bless