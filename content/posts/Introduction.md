+++
title = 'Introduction'
date = 2024-06-09T21:47:34-04:00
draft = false
type = "post"
tags = ["blog"]
+++

## Hello!

I'm Iris, full-time networking-developer-devopsec-whatever engineer, part-time writer, and cat enthusiast.   I decided to remake my personal webpage I made a few months on hugo, due to incredibly quick rendering speed and the ease of deployment.  

## My Approach

Hugo seemed like the next best approached to my Resume/Blog/Project/REDACTE website when I was initally considering redesigning everything.  I really didn't want to mess around with raw html and css, I'm not much of a frontend designer, but I am forcing myself to interact more with frontend elements.  So this seemed like the best compromise while I gain my bearings a bit.

### More specifically

I'm developing this current iteration in another branch in a repo that's currently hosting my singular Github Pages, static website.  The older iteration is using some very basic Jekyll, and it's pointed at irisshannon.dev.

I'll be following Hugo's Github Page [Deployment](https://gohugo.io/hosting-and-deployment/hosting-on-github/) guide in order to get this running in tip top shape.

## Issues I ran into

So the only kinda crudy thing about Hugo is the majority of public themes are riddled with bugs.  Bugs on bugs on bugs, stemming from basic HTML issues, to configuration issues due to how they setup functions within their base html templates. 

I started by using https://github.com/vaga/hugo-theme-m10c as my base, but slowly figured out there were some utterly strange theme configuration issues.  The vast majority of the color theme configurations only applied to the front page, and not the every page within content.  I fixed some of the issues, and a bit of stems from this being an old theme that's not currently being worked on.

So I moved to Poison.  Which was a lot better contructed, but I ran into similar issues https://github.com/lukeorth/poison/. When any markdown content files were in the root directory, the brand_image would work fine, but if you specify that a layer deep, it would fail to find the brand_image/avatar.  Which for me was a big deal because I commissioned art awhile back I intented to use.  I did some bug fixing on that, but honestly, I didn't really feel like fixing this immediately.

Finally I settled on the current theme gokarna.  Worked immediately out of the box.  Fantastic docuementation https://gokarna-hugo.netlify.app/posts/theme-documentation-basics/, and everything fit together well.

The feather icons were a nice touch, and easy to implement, and honestly, this might be the best documented theme outside of themes centered around being used for internal api documentation.

##  Moving Forward

Since I'm really trying to work on skills I sort of suck at right now I'm going to focus on projects that will help where I'm lacking:

Primary:
- Redesigning this website into a Svelete / Skeleton/Tailwind FrontEnd, with a Python backend.
- Utilize Circleci to automate an ArgoCD deployment of a few of these website.
    - Though this is a bit costly. Digital Ocean's Lowest tier is 24 dollars a month for a kube deployment

Secondary:
- Design a website for my penname, probably going to use hugo for easy auto deployment and blogging features.
- Work on projects with an empahsis on Javascript just because while I know it, I really don't use it minus a work project here or there.  I should be more comfortable in it to work on being a better fullstack developer

Certifications:
- Kubernetes Certification is my next big cert I'm going to grab. (looks nice from a recruitting front)
- Docker Cert (Same with the kube one, it looks good on a recruiting front)

Longterm Project:
- I've been thinking about ways make it easy for people to deploy and maintain communication platforms like discord, teamspeak, and forums.  Discord doesn't really allow for selfhosting, and there's a giant gap in the market for real forum interactions.  Reddit use to fill the niche, but doesn't anymore due to radical changes to make it more like a social network like FB or Instragram.
    - Ultimately something like this will be super difficult to undertake.
        - Forums themselves is a giant mess of badly optimized SQL calls on tables on tables and joins on joins
        - Discord primarily uses WebRTC, which is limited. I.E. That's why they only run on Electron right now.
        - Voip is messy.  WebRTC handles that for discord, but I aim to make it more like mumble.
    - Deployment of this is also kinda gross.  I want a mix between OpenSource functionality, and Premium functionality to make money on it.
    - Allowing for a universial account system (maybe something like an private / pub RSA key kinda thing for verification)
    - Needs to be very very secure if users want. 