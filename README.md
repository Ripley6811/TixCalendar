TixCalendar
===========

Calendar widget for Tix / Tkinter applications.

Based on ttk Treeview calendar but with improvements in pre-setting date and integration into other applications. Uses Tix if available for import or else uses Tkinter.

Can extend the length of the displayed month by prepending and appending additional weeks for display and selection.

Works with a StringVar for storing the selected date. A StringVar can be passed to the Calendar as a parameter or else it creates one internally. Use `date_str` or `date_obj` to retrieve the selected date from Calendar.

Usage:

    import Tix
    import calendar_radiobutton as cal
    
    mainf = Tix.Frame()
    # Creating a StringVar object is optional. Pass to Calendar as textvariable.
    date_SV = Tix.StringVar()
    cal = cal.Calendar(mainf, textvariable=date_SV, settoday=True)
    cal.pack()
    
    # To get a string representation of a date after selection access the StringVar or the date_str property of Calendar.
    date_SV.get()
    cal.date_str
    
    # To get a datetime.date object of the selected date access the date_obj property of Calendar.
    cal.date_obj

Todo:

- Fix month name encoding error when locale is on a Chinese system.
- Add optional Tix.Balloon popup over date buttons.
