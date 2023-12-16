# AdminFinder
This thing will find some goodies in your Web App Hacking Adventures. 
Hey there! So, what we've got here is a cool little Python script that's like a digital ninja for finding hidden admin panels on websites. It's designed to work its way through a massive list of potential secret paths (like "admin/", "administrator/", etc.) on a given website and see which ones actually exist.

Think of it as playing hide-and-seek with website paths. It's quite clever. It doesn't just knock on the front door (HTTP); it also checks the back door (HTTPS) for each path. It's like trying two keys for every lock.

The heart of the script is this team of threads – think of them as little digital minions. We've got a bunch of them (200 to be exact) working together. Each minion grabs a path and then scurries off to check if it's a real deal on the website, first under the 'http' disguise and then as 'https'.

While these minions are out and about, they’re super considerate and keep each other in the loop. They use this shared queue to pick their tasks and a shared session for making their web requests, which is pretty efficient and speeds things up.

As each path gets checked, the script makes a note of it. And, for the paths that do exist, it records what it found in a report file. It’s like each minion is sending postcards from the paths they discover.

To make sure we’re not just wildly guessing in the dark, there's this nifty progress bar that shows how far along we are in our path-finding mission.

And finally, once all the minions have finished their tasks, we get a nice summary of all the paths they found, highlighted with different colors based on whether they were successful or not. Green means "Eureka! Found something!", and yellow is more like a "Hmm, there's something here but not quite the jackpot."

So that's pretty much it – our own little cyber detective squad, sniffing out hidden paths and potentially uncovering some secret doors!
