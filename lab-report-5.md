Lab Report 5
=======
_Sravya Chittuluri_

I chose to redo lab report 3 to explore more commands and the different ways I could use them when working with the terminal. 
Last time, I chose the ```find``` command and found three different command-line options to alter how the command works: ```-iname```, 
```-atime```, and ```-size```.

For this lab, I wanted to do the same exploration but for the ```grep``` command.

***-r***

```-r```: finds given text in the folder or any of its subfolders (recursive search). This is useful to quickly go through multiple files to search for text instead of having to go through each file separately.

Input:

```
grep -r Honolulu travel_guides/*
```

Output:

```
travel_guides/berlitz1/HandRHawaii.txt:        Oahu (Including Honolulu)
travel_guides/berlitz1/HandRHawaii.txt:        Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
travel_guides/berlitz1/HandRHawaii.txt:        Halekulani $$$$ 2199 Kalia Road, Honolulu, HI 96815; Tel.
travel_guides/berlitz1/HandRHawaii.txt:        Hilton Hawaiian Village $$$–$$$$ 2005 Kalia Road, Honolulu,
travel_guides/berlitz1/HandRHawaii.txt:        Honolulu, HI 96815; Tel. (808) 923-1234 or (800) 233-1234; fax (808)
travel_guides/berlitz1/HandRHawaii.txt:        half-hour drive of Honolulu. 387 rooms.
travel_guides/berlitz1/HandRHawaii.txt:        Honolulu, HI 96816; Tel. (808) 739-8888 or (800) 367-2525; fax (808)
travel_guides/berlitz1/HandRHawaii.txt:        Outrigger Reef $$$ 2169 Kalia Road, Honolulu, HI 96815; Tel.
travel_guides/berlitz1/HandRHawaii.txt:        Pacific Beach Hotel $$$ 2490 Kalakaua Avenue,, Honolulu, HI
travel_guides/berlitz1/HandRHawaii.txt:        Royal Hawaiian $$$$ 2259 Kalakaua Avenue, Honolulu, HI
travel_guides/berlitz1/HandRHawaii.txt:        Honolulu, HI 96815; Tel. (808) 922-3111 or (800) 325-3535; fax (808)
travel_guides/berlitz1/HandRHawaii.txt:        Honolulu, HI 96815; Tel. (808) 922-5811 or (800) 325-3535; fax (808)
travel_guides/berlitz1/HandRHawaii.txt:        Sheraton Waikiki $$$–$$$$ 2255 Kalakaua Avenue, Honolulu,
travel_guides/berlitz1/HistoryHawaii.txt:        church and the mission schools (which you can still visit in Honolulu)
travel_guides/berlitz1/HistoryHawaii.txt:        Honolulu. The Calvinistic reforms were soon reversed when Kaahumanu
travel_guides/berlitz1/HistoryHawaii.txt:        still be toured in Honolulu. He also legalized the hula, Hawaii’s
travel_guides/berlitz1/HistoryHawaii.txt:        governor was Dole. Queen Liliuokalani lived out her life near Honolulu,
travel_guides/berlitz1/WhatToHawaii.txt:        Midway. Lying some 1,100 miles northwest of Honolulu, Midway
```

Here, the grep command recursively searches through all of the folders and subfolders inside of travel_guides to find every instance of Honolulu within the txt files. It returns the file names, as well as where Honolulu occurs in the txt file.

Input:

```
grep -r bewildered non-fiction/OUP/*
```
Output:

```
non-fiction/OUP/Berk/ch1.txt:baffled, bewildered parents
non-fiction/OUP/Berk/ch1.txt:Despite being well educated, intent on doing what’s best for their children, and enlightened by a vast literature of child-rearing advice, many American parents appear uneasy and unsure of their roles at best, baed and bewildered at worst. As the above sampling of concerns reveals, today’s parents are not just worried about major transitions and traumas, such as the impact of marital breakup or community violence. They agonize over commonplace, recurrent, everyday situations—whether intensive preschool academic tutoring is crucial for later success in school, the meaning of “quality time” with children, and whether and how to help their child with homework. At an even more fundamental level, contemporary parents have begun to doubt their own ecacy in their children’s development. Why is this so?
non-fiction/OUP/Kauffman/ch6.txt:And Gertrude flew! Yes, she flew away from the magnolia tree, eluding the bewildered Bertha. Later that month, Gertrude was married in a civil ceremony to a handsome squirrel, as she had become a heroine, was no longer shunned, and was considered a prize mate. Her odd flaps turned out to be a consequence of a simple Mendelian dominant gene, hence her kids had the same wondrous capacity to fly.
```

Here, the grep command does the same thing but searches through all of the files under non-fiction to find where 'bewildered' is used.

***-i***

```-i```: same functionality as the grep command, but is case insensitive. This is useful to find a specific string within a file without knowing the exact capitalization used in the file.

Input:

```
grep -i "palm beach hotel" travel_guides/berlitz1/HandRIsrael.txt
```

Output: 

```
Palm Beach Hotel and Country Club ❁❁-❁❁❁ Akko Beach; Tel.
```

Here, even though I didn't capitalize Palm Beach Hotel, the grep command still found the string.

Input:

```
grep -i "france and gerMANY" non-fiction/OUP/Fletcher/ch1.txt
```

Output: 

```
France and Germany
As France and Germany had their experiences of seeking redemption after reigns of terror, Americans, too, indulged in the mammoth bloodletting on the killing fields of the Civil War. When Lincoln sought to resupply Fort Sumter in Charleston harbor, and General Beauregard chose in response to fire on the federal fort, the long-simmering feud between North and South bled into brothers’ killing each other at close range. They fired their canons on Fort Sumter, they fixed their bayonets at Little Round Top, they lobbed shells onto Vicksburg until troops could seize the forts reigning over the Mississippi, they burned down Atlanta, and under William Tecumseh Sherman they scorched the earth on their march to the sea. The blue and the gray fell everywhere. And they were not sure why. They only had abstract ideas in their heads—some died for the Union, others for their separate nation. Over six hundred thousand lives stained the ground, more than all the former and subsequent American wars put together.
```

Here, even though I didn't properly capitalize France and Germany, the grep command still found the string.

***-l***

```-l```: only returns file names when looking inside files. Useful if you don't need all the specific locations of where the strings are in the files.

Input:

```
grep -rl Hawaii travel_guides/
```

Output: 

```
travel_guides/berlitz1/HandRHawaii.txt
travel_guides/berlitz1/HistoryHawaii.txt
travel_guides/berlitz1/HistoryMalaysia.txt
travel_guides/berlitz1/WhatToHawaii.txt
travel_guides/berlitz1/WhereToHawaii.txt
travel_guides/berlitz2/Bahamas-Intro.txt
travel_guides/berlitz2/California-History.txt
travel_guides/berlitz2/California-WhatToDo.txt
```

Here, I combined -r and -l for a recursive search for Hawaii in the files. It returned all the files that contained Hawaii, but only their file names.

Input:

```
grep -rl prognosis non-fiction/OUP/
```

Output: 

```
non-fiction/OUP/Abernathy/ch1.txt
```

Here, I also combined -r and -l for a recursive search for prognosis in the files. It only returned the file names where it found prognosis.

***-c***

```-c```: returns the names of files containing a given string and the number of hits in each file. This is useful if you want to know the frequency of the string within the file.

Input:

```
grep -c American non-fiction/OUP/Abernathy/ch1.txt
```

Output:

```
12
```

Here, the command returned how many times the string American was found inside the txt file.

Input:

```
grep -c hotel travel_guides/berlitz1/HandRLasVegas.txt
```

Output:

```
7
```

Here, the command returned how many times the string hotel was found inside the txt file.

