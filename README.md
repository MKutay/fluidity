my configs:
```text
[
  {
    "title": "Studies",
    "links": [
      {
        "label": "Notion",
        "value": "https://www.notion.so/mehmet-kutay-bozkurt/School-0d5a790f920349d6879dded502811961"
      },
      {
        "label": "TITC IA",
        "value": "https://docs.google.com/document/d/1KxdJVjJomRx5hOWguQan2KoE_szLd919J-H7wKm--l0/edit"
      },
      {
        "label": "TOK Exhibition",
        "value": "https://docs.google.com/document/d/1PTDHHrO9TK1Gceb94oVAzfNCsCk32LsPbhzqehVrv6w/edit"
      },
      {
        "label": "Managebac",
        "value": "https://oaal.managebac.com/student"
      },
      {
        "label": "BAL Blog",
        "value": "https://drive.google.com/drive/u/0/folders/1SLxuNocZJHvuhhmWvX8wXhoyQOuFVHw7"
      }
    ]
  },
  {
    "title": "Reddit",
    "links": [
      {
        "label": "r/ibo",
        "value": "https://www.reddit.com/r/ibo/"
      },
      {
        "label": "r/notion",
        "value": "https://www.reddit.com/r/notion"
      },
      {
        "label": "r/photography",
        "value": "https://www.reddit.com/r/photography/"
      },
      {
        "label": "r/mechanicalpencils",
        "value": "https://www.reddit.com/r/mechanicalpencils/"
      },
      {
        "label": "r/doctorwhumour",
        "value": "https://www.reddit.com/r/DoctorWhumour/"
      },
      {
        "label": "r/cats",
        "value": "https://www.reddit.com/r/cats"
      }
    ]
  },
  {
    "title": "Music",
    "links": [
      {
        "label": "music that i can listen 24/7",
        "value": "https://music.apple.com/library/playlist/p.V7VYpdDH4qKOW2X"
      },
      {
        "label": "howwy knight",
        "value": "https://music.apple.com/library/playlist/p.1YeWgmLf7AZo2W9"
      },
      {
        "label": "celeste",
        "value": "https://music.apple.com/library/playlist/p.ZOAX70eivOp7EAQ"
      },
      {
        "label": "new music",
        "value": "https://music.apple.com/tr/playlist/new-music-mix/pl.pm-8e975ad16716041c8c4ab89518260658"
      },
      {
        "label": "chill",
        "value": "https://music.apple.com/tr/playlist/chill-mix/pl.pm-8e975ad16716041c49a07ff6dd7ddbaf"
      }
    ]
  },
  {
    "title": "Sauce",
    "links": [
      {
        "label": "Kenkoooo",
        "value": "https://kenkoooo.com/atcoder/#/table/kuyta"
      },
      {
        "label": "Codeforces",
        "value": "https://codeforces.com/"
      },
      {
        "label": "Github",
        "value": "https://github.com/"
      },
      {
        "label": "best problem ever",
        "value": "https://atcoder.jp/contests/agc055/tasks/agc055_a"
      },
      {
        "label": "real sauce",
        "value": "https://github.com/FelixKratz/SketchyBar"
      },
      {
        "label": "da real sauce",
        "value": "https://github.com/koekeishiya/yabai"
      }
    ]
  }
]
```
pic: ./static/media/ign-0011.png
bg-color: #2e3440
def-color: #d8dee9
#acc-color: #81a1c1
#acc-color2: #5e81ac


![logo](https://github.com/PrettyCoffee/fluidity/blob/main/public/logo192.png)

# Fluidity - An accordion based startpage
Here you can find the startpage I created for my browser :)

If you have any problems or miss a feature, create an issue and I will take a look at it! Of course, if you want to add a feature yourself you can just create a fork and contribute ;)

## Showcase
### The startpage in action
I created a [reddit post](https://www.reddit.com/r/startpages/comments/m82izg/my_new_startpage_any_ideas_for_names/) on r/startpages. There you can see a short video where I show all available features.

You can also just take a look at the [Live Demo](https://prettycoffee.github.io/fluidity/).

### Themes
![Default theme](https://github.com/PrettyCoffee/fluidity/blob/main/docs/default-theme.png)
![Dark Souls theme](https://github.com/PrettyCoffee/fluidity/blob/main/docs/DarkSouls-theme.png)
![Pop!OS theme](https://github.com/PrettyCoffee/fluidity/blob/main/docs/pop!os-theme.png)
**If you created a theme and want to see it here, hit me up!**

## Usage
You can apply startpages by using several methods. To keep it simple, I will only cover one (the easiest) here:
1. Download a New Tab Override Plugin (e.g. [Chrome](https://chrome.google.com/webstore/detail/new-tab-redirect/icpgjfneehieebagbmdbhnlpiopdcmna) | [Firefox](https://addons.mozilla.org/en-US/firefox/addon/new-tab-override/))
1. Open the Plugins Settings
1. Paste `https://prettycoffee.github.io/fluidity/` into the text field to set it up as your startpage

## Local Setup
If you do not want to rely on my github page, thats totally okay!
You can set it up locally yourself with the following steps:
1. Switch into the gh-pages branch
1. Download / Clone the repository files
1. Set it up like explained in [usage](#usage), but instead of the link use the filepath to the `/index.html` file.

If you have a github account you can of course also just fork the repo and create a github page yourself ;)

## Docker setup
If you are familiar with Docker, you can use the provided docker file which will build the app and deploy it with nginx.

You can use the following commands to deploy a container:

```bash
# build
$ docker build ./ -t fluidity

# run
$ docker run -d --name fluidity -p 8080:80 fluidity
```

It will be deployed on port 8080. (`http:\\localhost:8080`)

## Advanced: Changing the code
Since this project is programmed with React and TypeScript, you will first need to set it up:

0. (Download and install [nodejs](https://nodejs.org/en/) if you dont have it)
1. Clone the git repository, this time use the main branch
1. Open a terminal in the project folder (If you execute the command `ls` here, there should be a package.json)
1. Execute `npm i` to install all dependencies
1. Execute `npm run start` to validate that everything ids working. A browser tab with the URL `http://localhost:3000` and the startpage should open.
1. Now you can change the code, for example write your own default values into `/src/data/data.ts`
1. Compile the project by executing `npm run build` if everything is done
1. Your startpage is now located in the `/build/` folder
1. Optional: If you host it with github pages yourself, you can use the command `npm run deploy` to push a fresh build into the gh-pages branch

## Sources

* [Pictures - DeathAndMilk](https://www.instagram.com/deathandmilk_/)
* [Icons - FontAwesome](https://fontawesome.com/icons)
* [Text Flicker - CodeMyUI](https://codemyui.com/crt-screen-text-flicker-animation-in-pure-css/)
* [Wave Animation - mburakerman](https://codepen.io/mburakerman/pen/eRZZEv)
