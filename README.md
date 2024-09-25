# CCBP-SQL-Assignment-1

Consider an online video-sharing platform like YouTube which hosts tens of thousands of channels and crores of users.

You have to analyse the data and provide meaningful insights on the type of content that drives engagement, users growth, and many more to all the stakeholders. Let’s roll our sleeves up for an insightful analysis!

Database
The sample database consists of tables that store the information of users, channels, videos, genres and likes/dislikes. 

Note:

channel_user table
channel_id	user_id	subscribed_datetime
100	1	2020-12-10 10:30:45
100	7	2020-10-10 11:30:45
...	...	...
channel_usertable stores the data of the channel_ids and their subscribers' user_ids.

First row in the table represents that the user with user_id = 1 is subscribed to the channel with channel_id = 100 at2020-12-10 10:30:45

user_likes table
user_id	video_id	reaction_type	reacted_at
1	10	LIKE	2020-12-10 10:30:45
7	10	DISLIKE	2020-10-10 11:30:45
...	...	...	...
Similarly, user_likestable stores the data of video_id and the user_ids who reacted to the video. A user can either like or dislike a video. He cannot like or dislike a video multiple times (similar to how youtube works)

video_genre table
video_id	genre_id
10	201
10	202
...	...
Similarly,video_genretable stores the data of video_id and the ids of the genres that the corresponding video belongs to. A single video can belong to multiple genres

Let’s dive in to analyze the in and outs of each part of the data. Here we go!

questions
1.
Get all the videos with more than 1 lakh views.

Note:
Output must be in the alphabetical order of videoname

Expected Output Format
video_id	name	duration_in_secs	published_datetime	no_of_views	channel_id
...	...	...	...	...	...
2.
Get videos from TEDx channel (id=353) with more than 50 thousand views.

Note:
Sort the output in the descending order ofno_of_viewsand in the ascending order of videoname

Expected Output Format
video_id	name	duration_in_secs	no_of_views
...	...	...	...
3.
Get the top 10 most viewed videos till date.

Note:
Sort the videos by no_of_views from highest to lowest. For videos with the same number of views, order them by published_datetime, with the most recent video first.

Expected Output Format
name	channel_id	no_of_views
...	...	...
4.
Get all the recent movie trailers that have more than 1 lakh views.

Note:
Consider the videos that have "trailer" in theirnameas trailers.
Sort the output in the descending order ofno_of_viewsandpublished_datetime
Expected Output Format
name	channel_id	no_of_views	published_datetime
...	...	...	...
5.
Get all the videos that are released in the year 2018. 

Note:
Sort the output in the descending order ofpublished_datetimeand then in the alphabetical order ofname

Expected Output Format
video_id	name	duration_in_secs	no_of_views
...	...	...	...
6.
Get the distinct ids of videos that belong to the following genres.

genre_id	genre
201	Comedy
202	Action
203	Thriller
211	Scifi
Note:
Sort the output in the descending order ofvideo_id

Expected Output Format
video_id
...
7.
Get all the esport videos that crossed one lakh views and were released between 2018 and 2020.

Note:
Consider the videos that have "esport" in theirname as gaming videos.
Sort the output in the descending order ofno_of_viewsandpublished_datetime
Expected Output Format
name	published_datetime	no_of_views
...	...	...
8.
Get the total number of channels in the database aschannels_count

Expected Output Format
channels_count
...
9.
Get the highest and least number of views for the videos in the database.

Expected Output Format
highest_number_of_views	least_number_of_views
...	...
10.
Get the average number of views for the videos released by the "Single Shot" Channel (id = 373)

Expected Output Format
avg_views
...
11.
Get the total count of premium users on the platform as premium_users_count.

Note - Consider those users as premium which has 1 in premium_membership column.

Expected Output Format
premium_users_count
...
12.
Get the number of male and female premium users in the platform.

Expected Output Format
gender	total_users
F	...
M	...
