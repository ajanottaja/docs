# Ajanottaja - A simple time keeping tool

> Try to imagine a life without timekeeping. You probably can’t. You know the month, the year, the day of the week. There is a clock on your wall or the dashboard of your car. You have a schedule, a calendar, a time for dinner or a movie. Yet all around you, timekeeping is ignored. Birds are not late. A dog does not check its watch. Deer do not fret over passing birthdays. an alone measures time. Man alone chimes the hour. And, because of this, man alone suffers a paralyzing fear that no other creature endures. A fear of time running out.
</br>― Mitch Albom, The Time Keeper


The name _Ajanottaja_ is the Finnish word for timekeeper.
It is chosen as a nod to the Finnish Clojure shop [Metosin's](https://www.metosin.fi/en/) [library](https://github.com/metosin) naming scheme, many of which is used in this project.

## Rationale

_Ajanottaja_ is a super simple time keeping tool built with the hubmle worker in mind.
Most time tracking solutions are built to help employers monitor employee work time.
Many of them feel over engineered or simply cludgy to use as an employee.
Ajanottaja is your friendly simple time keeper that will help you track your worked time.
Ajanottaja can tell you how many hours you are owed, or how many hours you've falled behind.
In time it will tell you which projects you worked on, but only if you want.

Some solutions try to automate the time tracking, Ajanottaja will simply do what you tell it to.
It won't care that you opened up that Twitter tab to rest your brain for five minutes, neither should anyone else.
It will not automatically detect that you started working on a new project.
Context switching is expensive, so you shouldn't do it more than once of twice a day anyway.

## Technology

Ajanottaja is built as a [backend API](https://github.com/ajanottaja/api) and [frontend single page app](https://github.com/ajanottaja/frontend) (SPA) stack.
A SPA was chosen because of the interactive timing functionality, and possibility of offline support.
The backend is a simple JSON over HTTP API built on top of [PostgreSQL](https://www.postgresql.org/) and [Clojure](https://clojure.org/).
Unlike some RESTful APIs the required data is not focused around statically shaped resources or entities.
Instead endpoints should deliver data fit for the given timing functionality needed.
In that respect Clojure's data orientation and PostgreSQL's powerful query support is a nice fit.