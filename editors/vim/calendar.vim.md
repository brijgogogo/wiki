= calendar.vim (itchyny) =

* :Calendar
* :Calendar 2000 1 1
* :Calendar -view=year
* :Calendar -view=year -split=vertical -width=27
* :Calendar -view=year -split=horizontal -position=below -height=12
* :Calendar -first_day=monday
* :Calendar -view=clock
* < and > : switch between views
* E : view events
* T : view tasks
* ? : quick help
* dd : delete event
* yy : yand event
* cc : change event
* a or i : add event
* u : undo
* L : redraw
* q : hide
* v : visual

== input format for events and tasks ==
EVENT: [event-title]
EVENT: HH:MM - HH:MM [event-title]
EVENT: yyyy/mm/dd - yyyy/mm/dd [event-title]
EVENT: mm/dd HH:MM - mm/dd HH:MM [event-title]
TASK: [task-title]
TASK: [task-title] note: [task-note]
TASK: mm/dd [task-title]
TASK: yyyy/mm/dd [task-title]
TASK: yyyy/mm/dd [task-title] note: [task-note]

