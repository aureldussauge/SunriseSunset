Sunrise Sunset
==============

This is a short C# file for calculating sunrise/sunset/twilight times (UTC), on a given day, at a given position.
This is the C# implementation of [Paul Schlyter's sunriset.c](stjarnhimlen.se/comp/sunriset.c).

Getting started
---------------

Get sunrise/sunset time and convert it to a string
````c#
double tsunrise, tsunset;
// Parameters : year - month - day - lat - long
Sunriset.SunriseSunset(2017, 2, 6, 46.214973, 5.241947, out tsunrise, out tsunset);
TimeSpan sunriseTime = TimeSpan.FromHours(tsunrise);
string sunriseTimeString = sunriseTime.ToString(@"hh\:mm\:ss");
Console.WriteLine(tsunrise+" "+sunriseTimeString);
```

Get civil/nautical/astronomical twilight times
````c#
double tsunrise, tsunset;
Sunriset.CivilTwilight(2017, 2, 6, 46.214973, 5.241947, out tsunrise, out tsunset);
Sunriset.NauticalTwilight(2017, 2, 6, 46.214973, 5.241947, out tsunrise, out tsunset);
Sunriset.AstronomicalTwilight(2017, 2, 6, 46.214973, 5.241947, out tsunrise, out tsunset);
```
