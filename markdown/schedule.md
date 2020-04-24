---
title: Spring 2020 Schedule
...

As this is my time teaching this course, I expect to change the flow and pacing of topics as the semester progresses.
The past, and my best guess of the future, is reflected below.

<hr/>

<style id="schedule-css">

#schedule.calendar {
    display: grid;
    width: 100%; 
    background: rgba(0,0,0,0.125); 
    border: 0.5ex solid rgba(0,0,0,0);
    border-radius: 1.5ex; 
}
.calendar .day.Sun { grid-column: 1}
.calendar .day.Mon { grid-column: 2}
.calendar .day.Tue { grid-column: 3}
.calendar .day.Wed { grid-column: 4}
.calendar .day.Thu { grid-column: 5}
.calendar .day.Fri { grid-column: 6}
.calendar .day.Sat { grid-column: 7}

.calendar .day { 
    background: white;
    border-radius: 1ex;
    padding: .25ex .5ex;
    margin: .25ex;
    box-sizing:border-box; 
    overflow: hidden;
}


#schedule td, #schedule th { padding: 0ex; }

.calendar span.date { 
    font-size: 70.7%;
    padding-left: 0.5ex;
    float:right;
    margin-top:-0.5ex;
}
.calendar div {
    padding: 0 0.5ex 0 0.5ex;
    margin: 0 -0.5ex 0 -0.5ex;
}
.calendar div.day div:first-child {
    padding-top: 0.5ex;
    margin-top: -0.5ex;
}
.calendar div.day div:last-child {
    padding-bottom: 0.5ex;
    margin-bottom: -0.5ex;
}


.agenda { display: block; }

.agenda .day.newweek {
    border-top: thick solid grey;
}
.agenda .day:not(.empty) {
    display: block; border-top: thin solid grey; width: 100%;
    padding: 0;
}
.agenda span.date.w0:before { content: "Sun "; }
.agenda span.date.w1:before { content: "Mon "; }
.agenda span.date.w2:before { content: "Tue "; }
.agenda span.date.w3:before { content: "Wed "; }
.agenda span.date.w4:before { content: "Thu "; }
.agenda span.date.w5:before { content: "Fri "; }
.agenda span.date.w6:before { content: "Sat "; }
.agenda span.date {
    font-size: 70.7%; width:7em;
    vertical-align: middle; 
    display: table-cell;
    padding: 0 0.5ex;
}
.agenda div.events { display: table-cell; vertical-align: middle; }

.assignment:before { content: "due: "; font-size: 70.7%; }
small { opacity: 0.5; }
.special, .exam { background: rgba(255,127,0,0.25); opacity: 0.75; }
span.date { font-family:monospace; }
details { padding-left: 1em; }
summary { margin-left: -1em; }

.day.past { opacity: 0.707; }
.day.today { box-shadow: 0 0 0.5ex 0.5ex grey; }
.agenda .day.today .wrapper { margin: 0.5ex 0;}

.calendar div.day.empty { background: rgba(0,0,0,0); padding: 0em; margin: 0em; border: none; border-radius: 0; min-height: 1.5em; }

</style>


<p>View as 
<label><input type="radio" name="viewmode" onchange="viewmode(this)" checked value="calendar" id="viewmode=calendar"> calendar</label>
or
<label><input type="radio" name="viewmode" onchange="viewmode(this)" value="agenda" id="viewmode=agenda"> agenda</label>;
<label><input type="checkbox" name="showpast" onclick="showPast(this)" checked id="showpast"> show past</label>;
readings can be <input type="button" value="shown" onclick="document.querySelectorAll('details').forEach(x => x.setAttribute('open','open'))"></input> or <input type="button" value="hidden" onclick="document.querySelectorAll('details').forEach(x => x.removeAttribute('open'))"></input> as a whole, or clicked on individually to toggle visibility.
</p>


{#include schedule.html}


<script src="schedule.js"></script>

To subscribe to the above calendar, add <http://www.cs.virginia.edu/luther/DMT1/S2020/cal.ics> to your calender application of choice.

<hr/>

Quiz 12 will be optional, a chance to make up one of the four topical areas.
All four areas will be available, but you will only be able to submit one (or none) of them.
It will be a 45-minute exam in the normal class time on the normal quizzing site.

The final exam will be on the day stated by the registrar, which is <a href="https://www2.virginia.edu/registrar/exams.html#1202">Thursday 30 April at 9:00 am</a>—to provide time-zone and related flexibility, we'll ignore the "9:00 am" part of that and give you 3 hours to take it anytime between 2020-04-30 00:00 EDT and 2020-04-30 23:59 EDT (once you start, you've got 3 hours to finish, and have to finish before 23:59).
All four areas will be available, and you can submit as many or few as you wish.
Those you do submit will be graded and replace your grade in the appropriate topics.
It will be administered via the normal quizzing site.

If you do not take a topic on either quiz, your score on that topic is unchanged. If you are satisfied with that score now, you do not need to take either Quiz 12 or the final.
