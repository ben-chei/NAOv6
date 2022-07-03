# NAOv6
Für den Kurs "Autonome Systeme"
Falls Catkin nicht installiert ist müsst ihr dies noch erledigen mit dem Befehl\\
$ source /opt/ros/kinetic/setup.bash (Dies erfordert die Zustimmung vom Admin deswegen holt euch einen Labormitarbeiter)
Als nächstes muss ein Catkin Workspace erstellt werden:

$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
Die Befehle nacheinander ausführen

Wenn das Workspace erstellt ist müsst ihr einen Setup Bash durchführen
$ source devel/setup.bash

Um sicherzustellen, dass euer Arbeitsbereich ordnungsgemäß vom Setup-Skript überlagert wird, stellt sicher, dass die Umgebungsvariable ROS_PACKAGE_PATH das Verzeichnis enthält, in dem ihr euch befindet

$ echo $ROS_PACKAGE_PATH
/home/youruser/catkin_ws/src:/opt/ros/kinetic/share

Als nächstes, müssen eure Python Skripts in dem Package abgelegt werden.
Für das durchführen der Python Skripts, müssen vorher noch einige Dinge durchgeführt werden:
In jedem Python Skript muss in der ersten Zeile folgendes stehen:
#! /usr/bin/env python
Speichert danach euer Skript.

Danach geht Ihr zurück zum Terminal:
Als erstes begebt Ihr euch, in das Catkin Package mit dem Befehl:
$ cd catkin_ws

Als nächstes müssen die Python Skripte für ROS ausführbar komprimiert werden:
Jedes Python SKript muss vorher mit dem folgenden Befehl im Terminal ausführbar bearbeitet werden:
chmod +x mypythonscript.py (für mypythonscript einfach mit dem Skript Namen ersetzen.)
Als letztes müsst Ihr jetzt die Skripte ausführen:
$ rosrun PackageName PythonSkriptName.py
