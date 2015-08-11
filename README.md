## Mobile developer competency test

#### Android. Question 1

- [ ] Suppose we starting a service in an Activity as shown below: 

```java
Intent service = new Intent(context, MyNetworkService.class);             
startService(service);
```

Imagine `MyNetworkService` accesses a remote server via Internet and the Activity shows an animation that indicates some 
kind of progress. Please, describe possible issue with this code?

- [ ] How would you address this issue?

#### Android. Question 2

- [ ] Please, describe the relationship between the life cycle of `AsyncTask` and `Activity`?
- [ ] Please, explain why it is generally a bad idea to use `AsyncTask` for a long-running background task?  

#### iOS. Question 1

- [ ] Please, explain why the code below logs "areEqual".

```objective-c
NSString *first = @"test";
NSString *second = @"test";


if (first == second)
{
  NSLog(@"areEqual");
}
else
{
  NSLog(@"areNotEqual");
}
```

#### iOS. Question 2

- [ ] Given you need to record an application launch time. So you created a class that defines a global variable in its header: 
`NSString *startTime;`. And in the class implementation, you set the variable as shown below:

```objective-c
+ (void)initialize {
  NSDateFormatter *formatter = [[NSDateFormatter alloc] init];
  [formatter setDateStyle:NSDateFormatterNoStyle];
  [formatter setTimeStyle:NSDateFormatterMediumStyle];
  startTime = [formatter stringFromDate:[NSDate date]];
}
```

Now you need to log the launch time in `application:didFinishLaunchingWithOptions:` method of your `AppDelegate`:

```objective-c
NSLog(@"Application was launched at: %@", startTime);
```

Please, explain why `null` will be logged?

- [ ] Please, suggest a fix how to solve this issue.

#### Practice. Mobile app.

Create an account at http://www.football-data.org/. 
Use [the API](http://api.football-data.org/docs/latest/index.html) to build a simple mobile application (iOS or Android). 

See below the API endpoints you need to use:

- [ ] `GET http://api.football-data.org/alpha/soccerseasons`: Returns a list of all seasons.
- [ ] `GET http://api.football-data.org/alpha/soccerseasons/{season_id}/fixtures`: Returns results of all matches in a specific season.
 
Please, implement 2-screens-application:

- [ ] `Screen 1. Seasons list`: List all seasons here. Go to the specific season on tap. 
- [ ] `Screen 2. Season results`: List all results in the specific season. 

Please, implement search filter on the `Season results` screen:

- [ ] The filter should consider both `Team A` and `Team B` names.

## Instructions

- Please, clone this repo in a new `Bitbucket` private repo.
- Edit `README.md` file to provide answers on first 4 tasks. 
- Implement a mobile app described in Task 5 and push your changes.
- Put in the repo short documentation on how to run the app using an emulator.
- Grant access to your private repo for BitBucket user `supertag` so we can review your code. 

We suppose this test require from 3 to 4 hours. Thanks in advance for your time spent on this test! 