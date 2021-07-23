---
layout: layouts/post.njk
title: adding CSS to my 11ty blog
description: until today, the blog had only default browser styles...now I can
  use my own CSS
date: 2021-07-22T04:00:00.000Z
featuredImage: /images/uploads/11ty-balloon.png
---
Hello!

I haven't had any updates in quite a few weeks, although I've been working on and studying other webdev topics.  I even published my first React project, [](https://rsrbmi.netlify.app/)[a BMI calculator](<https://rsrbmi.netlify.app/>).  But enough about that, I need to keep working on the blog.\
\
So today I set out to add at least a bare minimum of styling to the site.  Some layout, some font and background colors.  Oh, and a working nav bar.  \
\
I edited my base layout - I discovered I hadn't even really done the minimal HTML page boiler plate previously - and added a link to my CSS file, and some sematic markup which had been lacking previously.\
\
When I ran the dev server to check it out, I got my new HTML, but no CSS.  Hmmmm.  What I am I forgetting.  Nothing that a quick google couldn't solve - we need to tell 11ty any folders we want passed through to the published site.  Essentially the public folder in other systems.  \
\
Cool, got it.  I added `eleventyConfig.addPassthroughCopy("css");` to my `.eleventy.js` file, reloaded, and, I lose, I get nothing, good day, Sir!  What is happening?!?  Read, read, read, check, check, reload, reload.  Huh.  Still no CSS.  The folder is not being pushed to the public site folder, although the other two 'public' folder are as they have been.\
\
And then!  I see it!  I did not create my CSS folder in the root of the project.  That VS Code folder tree plays tricks on my eyes sometimes.  So I moved my CSS to the root, published and voilà, let there be styling.\
\
So that's the long story.  The short story is I used the normalize css package to 'reset' the css across browsers and have added a bare about of css to adjust the layout and colors.  I haven't even picked out any decent fonts yet.  But that's some research for tomorrow I suspect.\
\
TTYL,\
RSR