## Password Recovery, SC16

Anonymized results of passwords recovered from SC16 Password Recovery 

Some background for the uninitiated - These were recovered during the
Student Cluster Competition at SC16 in Salt Lake.  Auditing a large
password hash corpus was one of the competition applications. Students
run a number of applications for 48 hours on clusters with a power
limit of 3120 watts.

The hash corpus they got was generated from a number of dictionaries
of languages and compromised passwords, along with some rules applied
to permute words. It contained about 1 million md5 hashes, and about 2
million blowfish hashes, of various rounds of blowfish.  They had been
told that the competition data set would be at least partially
dictionary based and representative of user passwords, but not what
dictionaries they would be based on.

There were 3400944 total hashes in the competition data set. Across
all the teams 645873 distinct password hashes were cracked. 616330 of
those were MD5, 29543 were Blowfish.

The most successful team at this application got over 500,000
passwords, mostly md5, using nvidia p100 GPU's. Their technique was to
take a small random sample of the passwords to run a large number of
dictionaries over, and compare how many passwords were recovered using
each dictionary.  The dictionaries showing the best performance were
then used against the entire data set for the rest of the competition.
