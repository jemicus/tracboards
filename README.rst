tracboards - Trac dashboards
============================

tracboards is a collection of TV dashboards used by the Truveris Corps of
Engineers.

Configuration
-------------
To enable and configure tracboards, you need to  add the following to your
Trac configuration file::

    [components]
    tracboards.* = enabled

In addition, you can do some customization on a per-dashboard basis::

    [tracboards]
    defects.ticket_type = Defect

Installation
------------
Build an .egg file and drop it in the plugins directory of your Trac
installation::

    python setup.py bdist_egg

Defect Dashboard
----------------
This dashboard has two panels tracking the state of defects in your trac
project.  The left panel shows all the new and triaged open defects across all
components and milestones with a leader board of the components.  The right
panel shows all the tickets that were closed in the active milestones (with a
due date and no completion date) and a leader board of who closed these
tickets.

Configuration options::

    [tracboards]
    # Use this if your defect tickets have a different name:
    defects.ticket_type = Defect

Screenshot:

.. image:: https://s3.amazonaws.com/truveris-tracboards-assets/screenshots/defects.png