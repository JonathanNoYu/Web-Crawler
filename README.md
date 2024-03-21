### Approach
I initally thought of creating a get request function and post request function. Then once I get the log in stuff to work <br>
I would then go get every html page and parse all links and for possible flags. To keep track of links I thought of creating<br>
two lists one for visited and one for yet to visit (before I used a dictionary but thought a list would be faster to use).<br>
To add a new link I check if the link is a relative path and there is no @ symbol. I used a set for holding the flags <br>
since it is easy to check for duplicates. Lastly I found/use the HTMLParser to check starting tags and the data each tag <br>
has making it easy to get the flags and links. <br>

### Challenges
This project was difficult but there were times were I was lost and had to google a lot to figure out where I messed up <br>
Having port 80 for debugging was amazing since I figured out my isse with the host header through that. <br>
I did not optimize my code so figuring out if I could get all the flags was a bit of a challenge. All I did <br>
to figure it out is leave my program running for while (I think it was ~19.17 minutes) and I found them all <br>

### Testing
To test my code I ran it incrementally. As in I set up the get method with the loging page and once I ran my file and it <br>
was able to do get the page I added the other functionalities slow. Like parsing the csrftoken, the sessionid, Posting <br>
data, checking if I get valid links, then finally running it until I see flags. To debug I printed all the headers plus <br>
the request I sent to the console. I used import time on one run and it took 1147.9022336006165 seconds or 19.1317038933436083 minutes <br>