# Welcome to EduArt's repository overview
On this page you will find the documentation of the software packages for our robots as well as project-related repositories.
You will also find a quick guide and short instructions for our standard products here.

## Actively maintained robot repositories
### edu_robot
General interface description for all EduArt robots. Docker images are available to control our robots.  

Link: [edu_robot](https://github.com/EduArt-Robotik/edu_robot)

### edu_robot_control_template
This template code can be used as an example of how programs can be created to control EduArt robots and query their sensor values. 

Link: [edu_robot_control_template](https://github.com/EduArt-Robotik/edu_robot_control_template)

### edu_nodered_ros2_plugin
Descripiton and example of how to use a low code environment (block programming) on the robot.

Link: [edu_nodered_ros2_plugin](https://github.com/EduArt-Robotik/edu_nodered_ros2_plugin)


### iotbot
ROS interface for the IOTBot. Description of the hardware interfaces. This repository is still up-to-date for a ROS-based installation. If you want to use ROS2, it is better to switch to edu_robot.  

Link: [iotbot](https://github.com/EduArt-Robotik/iotbot)

### iotbot-ros2
ROS2 port of the iotbot repository. This repository contains only documentation and is used by idividual customers. If you want to use it, please drop a message at info@eduart-robotik.com.

Link: [iotbot-ros2](https://github.com/EduArt-Robotik/iotbot-ros2)

### edu_docker
Provides Dockerfiles for all EduArt's robots including deployment and launch scripts.

Link: [edu_docker](https://github.com/EduArt-Robotik/edu_docker)

## Utility repositories
Useful tools for controlling our robots.


### edu_virtual_joy
Virtual joystick based on Python3. There is a version for ROS and ROS2, which can be used for all robots that process a message of type geometry_msgs/Twist.  
Link: [edu_virtual_joy](https://github.com/EduArt-Robotik/edu_virtual_joy)
### joystick_drivers
Forked from ros-drivers/joystick_drivers (Convinience copy)  
Link: [joystick_drivers](https://github.com/EduArt-Robotik/joystick_drivers)



## Perception repositories
This section contains higher-level algorithms that can be useful for (semi-)autonomous operation.
### edu_perception
Various software algorithms for the detection of objects. Only one QR code detector is currently implemented/referenced.  
Link: [edu_perception](https://github.com/EduArt-Robotik/edu_perception)
### edu_swarm
Extension package to control several robots synchronously.  
Prerequisite: All robots require a precise localization concept.  
Link: [edu_swarm](https://github.com/EduArt-Robotik/edu_swarm)

## Project-related repositories
### edu_robocup_rescue_stack
Public benefit repository, that contains software that is useful for the RoboCup in the discipline of rescue robotics.  
Link: [edu_robocup_rescue_stack](https://github.com/EduArt-Robotik/edu_robocup_rescue_stack)
### robotsunite
This educational project promotes inter-school collaboration in a scenario similar to rescue. Each school develops an individual robot and challenging obstacles / tasks. No single robot can solve the given tasks alone. Thus, student teams from several schools must join forces.  
You can find our project wiki here: [Wiki](https://github.com/EduArt-Robotik/robotsunite/wiki)  
Link: [robotsunite](https://github.com/EduArt-Robotik/robotsunite)


# Deutsch
## Schnellstart
Diese Anleitung soll nur helfen, die Erstinbetriebnahme des Roboters zu erleichtern. Nähere Beschreibungen finden Sie in den einzelnen Repositorys (oben verlinkt). 
Im Auslieferungszustand läuft auf dem Roboter bereits Software, die das direkte Steuern des Roboters mit dem PlayStation®5-Controller zulässt (natürlich nur, wenn dieser dazu gekauft wurde) und kein vorheriger Benutzer etwas umgestellt hat. Er ist auch bereits mit dem Roboter verbunden worden. Falls der Controller nicht verbindet, wurde ggf. das USB-Kabel zum USB-Hub nicht eingesteckt 😉. Dieses kann unter Umständen durch das Lagern in den Roboter gerutscht sein. Falls das immer noch nicht hilft, gehen Sie den Abschnitt PS5-Controller unter [edu_robot]( https://github.com/EduArt-Robotik/edu_robot/blob/main/documentation/setup/joystick/ps5-gamepad.md).
1.	Platzieren Sie den Roboter auf dem Lagergestell.
2.	Schalten Sie den Roboter ein. Dafür kippen Sie den Ein-Schalter auf die Stellung „I“. Drücken Sie dann den Ein-Taster ca. 2s
3.	Warten Sie ca. 30s, bis alles hochgefahren ist. Sie erkennen das daran, dass die Beleuchtung aufhört zu pulsieren und weiß rotiert (oder grün blinken, falls das Ladegerät gesteckt ist).
4.	Schalten Sie den PS5-Controller ein. Drücken Sie hierzu auf den „PS“ Knopf in der Mitte.
5.	Testen Sie nun anhand einiger Beleuchtungswechsel, ob der alles funktioniert. Z.B. „L1“ dann sollte der Roboter links blinken. 
6.	Ziehen Sie, falls vorher gesteckt, das Ladekabel ab und entriegeln Sie den Not-Halt (Sie sollten sehen, dass ein Licht an der Platine an- und ausgeht, wenn du der Not-Halt-Schalter betätigt wird)
7.	Setzten Sie den Roboter auf dem Boden ab (nicht auf einem Tisch!).
8.	Drücken den „Options“-Knopf (kleiner Knopf links neben dem „Dreieck“), um ein „Enable“ zu schicken (nun leuchten zwei Lampen an der Platine)
9.	Fahren Sie umher, ohne den Roboter dabei Treppen oder andere Abgründe herunterzustürzen. Das mag er gar nicht! Sie können nun nicht nahe an eine Wand fahren. Sehe im Kapitel „Roboter Steuern“ mehr darüber, wie Sie diese Sicherheitsfunktion abschalten können.

### Mit dem PC auf einem Roboter verbinden
Wenn man sich mit dem Roboter verbunden hat, kann man z.B. eigene Programme erstellen, mit NodeRed arbeiten, den Roboter mittels Weboberfläche steuern.
Verwenden Sie wenn vorhanden am besten den Standardrouter auf dem Roboter. Dieser spannt ein WLAN auf, auf das man sich aufschalten kann.
Wenn der Router nicht verstellt wurde, stimmt die SSID und das Passwort (auch Admin) überein. Falls der Router verstellt wurde, kann dieser zurückgesetzt werden, indem der Resetknopf gedrückt wird (näheres finden Sie in der Anleitung des Routers: TP-Link TL-WR802N).
Die Standard-IP-Adresse des PCs auf dem Roboter lautet 192.168.0.100.

### SSH-Verbindung aufbauen
Eine SSH-Verbindung wird benötigt, um auf das System eines externen PCs zu gelangen, um dort Änderungen vornehmen zu können.
Öffnen Sie eine Kommandozeile entweder in Windows („Windows-Taste“  „cmd“  Enter), oder in Linux („Strg.“ + „Alt“ + „T“). 
Sie kommen auf den Roboter je nach Konfiguration entweder oder mit dem folgenden Befehl (Voraussetzung ist, dass die [Inbetriebnahme]( https://github.com/EduArt-Robotik/edu_robot/blob/main/documentation/setup/iot2050/setup_iot2050.md) ausgeführt wurde). In der Standardkonfiguration ist das für Sie bereits von uns eingerichtet. 

```bash
ssh user@192.168.0.100
```
Das Passwort lautet „eduart“.

> **_Hinweis:_** Sie sehen keine Sternchen beim Tippen!

### Den Roboter mit dem Internet verbinden
Um neuen Code, oder Updates auf den Roboter zu laden muss er mit dem Internet verbunden sein (man könnte auch Ordner über Programme wie „Filezilla“ offline kopieren). Auch zum Starten von neuen Docker-Containern ist eine Internetverbindung notwendig. 
Je nachdem in was für einer Einrichtung Sie mit dem Roboter arbeiten kann dies eine leichte oder eher schwere Aufgabe sein (ziehen Sie zur Not Ihren IT-Admin zurate). Sitzen Sie z.B. im Home-Office, ist das meist kein Problem. 
Die leichteste Möglichkeit den Roboter mit dem Internet zu verbinden ist ihn, direkt per LAN-Kabel am Router anzustecken. Über die Benutzeroberfläche des Routers können Sie dann die IP-Adresse herausfinden. Alternativ können Sie in Linux und Windows den nmap-Befehl ausführen: 
```bash
nmap -sP 192.168.178.1/24
```
Stellen Sie vorher sicher, in welchem Adressraum Sie sich befinden. Das geht unter Windows über 
```bash
ipconfig
```
und in Linux über
```bash
ip a
```
Eine ***grafische Möglichkeit** bietet das Programm Advanced IP Scanner in Windows. Tragen Sie hier in der oberen Leiste die Adressbereiche ein, in denen Sie suchen möchten (z.B. 192.168.178.1-254). 

Als alternative Möglichkeit den Roboter mit dem Internet zu verbinden, bietet es sich an, den Router auf dem Roboter umzukonfigurieren. Hierbei ist allerdings darauf zu achten, dass die Fehlersuche für den nächsten Benutzer etwas unschön werden kann, wenn er oder sie versucht sich auf das Netzwerk des Roboters zu verbinden. Sie gelangen auf die Benutzeroberfläche des Routers, indem Sie sich mit dem WLAN des Routers verbinden und in einem Browser Ihrer Wahl die IP-Adresse des Routers eingeben (192.168.0.1). Dort können Sie dann den Quick-Setup-Wizzard ausführen und den Router als „Client“ konfigurieren.

### Warum GitHub
Mit GitHub arbeiten weltweit unzählige Unternehmen, Forschungseinrichtungen und Privatpersonen. GitHub ist eine webbasierte Plattform zur Versionsverwaltung und kollaborativen Softwareentwicklung, die Git als Versionskontrollsystem verwendet. Wir verwenden GitHub für Tutorials, Beispielcode und den Hauptcode, der die Roboter ansteuert. In regelmäßigen Abständen durch unsere Beispiele zu sehen lohnt sich, da diese stetig erweitert werden.

**Die wichtigsten Git-Befehle**
Um überhaupt ein Repository auf einen PC herunterladen zu können, nutzt man den „clone“ Befehl. 
z.B. 
```bash
git clone https://github.com/EduArt-Robotik/edu_robot_control_template
```
um unser Beispielrepository für c++ und Python herunterladen zu können. Alternativ kann man auch über die Webseite von GitHub den Code direkt als .zip Ordner herunterladen.

Falls ein Mitarbeiter von uns sagt: Machen Sie mal ein Update! So verwenden so wechseln Sie in den Ordner, in dem das Repository liegt, z.B.:
```bash
cd ~/edu_robot_control_template
```
und führen dort den „pull“-Befehl aus. 
```bash
git pull
```
Falls Sie etwas in den Dateien geändert haben müssen Sie (bei eigenen Repositorys) zunächst einen „commit“-Befehl durchführen. In dem Fall, dass Sie EduArt Standardrepos verwenden (und wir nicht empfehlen dort etwas zu ändern, sondern für Änderungen eigene Repos zu erstellen, um updatefähig zu bleiben) nutzen Sie den „stash“-Befehl (**Achtung alle Ihre Änderungen sind dann gelöscht**)
```bash
git stash
```
gefolgt vom „pull“-Befehl 😉

Wenn Sie sehen wollen, was sie alles geändert hatten, um zu sehen, ob das „wichtig“ ist und gespeichert werden sollte, verwenden Sie den „diff“-Befehl:
```bash
git diff
```

### Warum Docker
Docker ist eine Open-Source-Plattform, die es ermöglicht, Anwendungen in Containern zu verpacken, zu verteilen und auszuführen. Container kann man sich vorstellen wie abgespeckte virtuelle Maschinen. Wir benötigen das für unsere Roboter, um z.B. ROS2 auf Systemen laufen zu lassen, auf denen das nur schwer manuell zu installieren wäre. Zudem können so recht einfach Updates gefahren werden und einzelne Funktionen hinzugeschaltet werden.

**Die wichtigsten Docker-Befehle**
Wenn Sie mit dem Roboter verbunden sind, können Sie recht einfach sehen, welche Docker-Container gerade aktiv sind. Verwenden Sie hierzu den „ps“-Befehl:
```bash
docker ps
```
Es wird Ihnen so auch angezeigt, ob ein Container evtl. ein Problem mit dem Starten hat.

Um in einen Container hineinzuwechseln, verwenden Sie den Befehl (vervollständigen Sie die Eingabe des Containernamens mit der Tap-Taste):
```bash
docker exec -it <Containername> bash
```

Nun sind Sie im Container. Um dort ROS2 Topics zu sehen und diese entsprechend zu beobachten, führen Sie den folgenden Befehl aus:
```bash
source install/setup.bash
```
gefolgt von
```bash
ros2 topic list
```
> **_Hinweis:_** Gegebenenfalls müssen Sie den „list“ Befehl ein zweites mal ausführen um alle Topics sehen zu können.

Um einen Container zu stoppen, verwenden Sie den Befehl (den Containernamen können Sie mit der Tap-Taste vervollständigen lassen)
```bash
docker stop <Containername>
```
Um einen Container dann zu löschen (das müssen Sie nicht unbedingt) verwenden Sie den „rm“-Befehl (**Achtung, alle Änderungen, die zuvor im Container vorgenommen wurden, sind damit gelöscht**):
```bash
docker rm <Containername>
```

Im Normalfall sind die Repositorys von EduArt so strukturiert, dass im Repo ein „docker“ Ordner liegt. Um nun also einen EduArt-Docker-Container zu starten, müssen Sie in diesen Ordner wechseln. Also z.B. für edu_robot wie folgt:
```bash
cd ~/edu_robot/docker
```
Dort sind dann, falls es systemspezifische Abhängigkeiten gibt, verschiedene Ordner für verschiedene Computer wie z.B. das IOT2050. Wechseln Sie in den Ordner, den Sie benötigen 
```bash
cd iot2050
```
Dort können Sie nun einen EduArt Container **starten** (achten Sie darauf, dass es nötig sein kann, dass der Roboter auch hier noch Zugang zum Internet hat).
```bash
docker compose up
```

### Updates erhalten
In allen Repos ist der Prozess des Updatens beschrieben. Hier nochmal eine Kurzfassung (der Roboter oder das zu updatende System muss Internetzugriff haben!):
1.	Mit dem Roboter per SSH verbinden (dieser Schritt kann übersprungen werden, falls sich der Code auf dem eigenen System wie z.B. Laptop befindet)
2.	An den Ort wechseln, an dem das Repo auf dem PC, im Roboter, oder in der virtuellen Maschine o.Ä. liegt und in den Ordner gehen z.B.:
```bash
cd ~/edu_robot/
```
3.	Den neusten Code herunterladen:
```bash
git pull
```
> **_Hinweis:_** falls hier eine Fehlermeldung wg. vorhandenen Änderungen angezeigt wird sehen Sie hier im Kapitel „Warum GitHub“ wie Sie dieses Problem lösen können. Achten Sie darauf wichtige Änderungen vorher zu sichern.
4.	In den entsprechenden Docker-Ordner wechseln, z.B.:
```bash
cd ~/edu_robot/docker/iot2050/ 
```
5.	Neuen Docker-Container starten:
```bash
docker compose up
```
6.	Evtl. alten Container löschen (siehe Kapitel „Warum Docker“)


### Beispielanwendungen
Sehen Sie die verlinkten Repositorys oben, auf welche Beispielcodes Sie zurückgreifen können.
Für **Beginner** empfehlen wir zunächst mit dem Steuern über den PS5-Controller zu starten. Danach sollte man z.B. das [NodeRed Beispiel] (https://github.com/EduArt-Robotik/edu_nodered_ros2_plugin) durcharbeiten. Daraufhin kann man sich ansehen, wie das „Don’t hit the wall“-Beispiel in NodeRed auch in c++ oder Python umgesetzt werden kann. Dies findet man in unserem [edu_robot_control_template] (https://github.com/EduArt-Robotik/edu_robot_control_template). Daraufhin können Sie Ihren eigenen Code erstellen. Wir empfehlen entweder nativ auf ROS2 in einer virtuellen Maschine auf Ihrem System zu arbeiten, oder auf dem Roboter eigene Docker-Container zu erstellen. Kopieren Sie hierzu alle nötigen Dateien, z.B. aus unserem [edu_robot-Repository] (https://github.com/EduArt-Robotik/edu_robot/tree/main/docker/iot2050). Dies ist allerdings schon eher Expertenwissen.


# English
### Quick start
These instructions are only intended to help with the initial commissioning of the robot. More detailed descriptions can be found in the individual repositories (linked above).
When delivered, the robot is already running software that allows the robot to be controlled directly with the PlayStation®5 controller (of course only if this has been purchased) and no previous user has changed anything. It has also already been connected to the robot. If the controller does not connect, the USB cable to the USB hub may not be plugged in 😉. This may have slipped into the robot during storage. If this still does not help, go to the PS5 controller section in [edu_robot]( https://github.com/EduArt-Robotik/edu_robot/blob/main/documentation/setup/joystick/ps5-gamepad.md).
1.	Place the robot on the storage rack.
2.	Switch on the robot. To do this, tilt the On switch to the "I" position. Then press the On button for approx. 2s
3.	Wait approx. 30s until everything has started up. You can recognise this by the fact that the lighting stops pulsating and rotates white (or flashes green if the charger is plugged in).
4.	Switch on the PS5 controller. To do this, press the "PS" button in the centre.
5.	Now test whether everything works by changing the lighting a few times. E.g. "L1" then the robot should flash on the left. 
6.	Unplug the charging cable, if previously plugged in, and unlock the emergency stop (you should see a light on the circuit board go on and off when you press the emergency stop button)
7.	Place the robot on the floor (not on a table!)
8.	Press the "Options" button (small button to the left of the "triangle") to send an "Enable" (now two lights on the circuit board light up)
9.	Drive around without throwing the robot downstairs or other precipices. He doesn't like that at all! You cannot drive close to a wall now. See the chapter "Controlling the robot" for more information on how to switch off this safety function.#

### Connect to the PC on a robot
Once you have connected to the robot, you can, for example, create your own programmes, work with NodeRed and control the robot via the web interface.
If available, it is best to use the standard router on the robot. This will set up a WLAN that you can connect to.
If the router has not been adjusted, the SSID and password (also Admin) will match. If the router has been changed, it can be reset by pressing the reset button (for more information, see the router manual: TP-Link TL-WR802N).
The default IP address of the robots PC is 192.168.0.100.

### Establish SSH connection
An SSH connection is required to access the system of an external PC in order to make changes there.
Open the command line either in Windows (“Windows key”  “cmd”  Enter), or Linux (“Ctrl” + “Alt” + “T”).
Depending on the configuration, you can access the robot either or with the following command (provided that [Setup]( https://github.com/EduArt-Robotik/edu_robot/blob/main/documentation/setup/iot2050/setup_iot2050.md) has been executed). We have already set this up for you in the standard configuration.

```bash
ssh user@192.168.0.100
```
The password is “eduart”.

> **_Note:_** You will not see any asterisks when typing!

### Connect the robot to the internet
To upload new code or updates to the robot, it must be connected to the Internet (you could also copy folders offline using programmes such as "Filezilla"). An internet connection is also required to start new Docker containers.
Depending on the type of organisation in which you work with the robot, this can be an easy or rather difficult task (consult your IT admin if necessary). If you are working from home, for example, this is usually not a problem.
The easiest way to connect the robot to the Internet is to connect it directly to the router using a LAN cable. You can then find out the IP address via the router's user interface. Alternatively, you can run the nmap command in Linux and Windows:
```bash
nmap -sP 192.168.178.1/24
```
Make sure beforehand which address space you are in. This can be done under Windows via
```bash
ipconfig
```
or under Linux
```bash
ip a
```
The Advanced IP Scanner programme in Windows offers a ***graphical option**. Enter the address ranges in which you want to search in the top bar (e.g. 192.168.178.1-254).
An alternative way to connect the robot to the internet is to reconfigure the router on the robot. However, it should be noted that troubleshooting for the next user can be a bit messy if he or she tries to connect to the robot's network. You can access the router's user interface by connecting to the router's WLAN and entering the router's IP address (192.168.0.1) in a browser of your choice. You can then run the quick setup wizard and configure the router as a "client".

### Why GitHub
GitHub is used by countless companies, research organisations and private individuals worldwide. GitHub is a web-based platform for version management and collaborative software development that uses Git as its version control system. We use GitHub for tutorials, sample code and the main code that drives the robots. It's worth looking through our examples at regular intervals, as they are constantly being expanded.

**The most important Git commands**
The "clone" command is used to download a repository to a PC.
e.g.
```bash
git clone https://github.com/EduArt-Robotik/edu_robot_control_template
```
to download our example repository for c++ and Python. Alternatively, you can also download the code directly as a .zip folder from the GitHub website.
If one of our employees says: Do an update! To use this, change the folder in which the repository is located, e.g:
```bash
cd ~/edu_robot_control_template
```
and execute the pull command there
```bash
git pull
```
If you have changed something in the files, you must first execute a "commit" command (for your own repositories). In case you use EduArt standard repos (and we do not recommend to change anything there, but to create your own repos for changes in order to remain updatable) use the "stash" command (**beware all your changes are then deleted**)
```bash
git stash
```
followed by the "pull" command 😉

If you want to see what you have changed to see if it is "important" and should be saved, use the "diff" command:
```bash
git diff
```

### Why Docker
Docker is an open source platform that enables applications to be packaged, distributed and executed in containers. Containers can be thought of as slimmed-down virtual machines. We need this for our robots, for example to run ROS2 on systems on which it would be difficult to install manually. It also makes it very easy to run updates and add individual functions.

**The most important Docker commands**
If you are connected to the robot, you can easily see which Docker containers are currently active. Use the "ps" command to do this:
```bash
docker ps
```
This will also show you whether a container may have a problem with starting.

To switch into a container, use the command (complete the entry of the container name with the tap button):
```bash
docker exec -it <Container name> bash
```

You are now in the container. To see ROS2 topics there and monitor them accordingly, execute the following command:
```bash
source install/setup.bash
```
followed by
```bash
ros2 topic list
```
> **_Note:_** You may have to execute the "list" command a second time to see all topics.

To stop a container, use the command (you can complete the container name with the tap button)
```bash
docker stop <container name>
```

To delete a container (you do not necessarily have to do this), use the "rm" command (**note that all changes previously made in the container will be deleted**):
```bash
docker rm <container name>
```
Normally, the EduArt repositories are structured in such a way that there is a "docker" folder in the repo. To start an EduArt docker container, you must change to this folder. For edu_robot, for example, as follows:
```bash
cd ~/edu_robot/docker
```

If there are system-specific dependencies, there will be different folders for different computers, such as the IOT2050. Change to the folder that you need
```bash
cd iot2050
```

There you can now **start** an EduArt container (please note that it may be necessary for the robot to still have access to the Internet here).
```bash
docker compose up
```

### Receive updates
The update process is described in all repos. Here is a short version (the robot or the system to be updated must have internet access!):
1.	Connect to the robot via SSH (this step can be skipped if the code is located on your own system, e.g. laptop)
2.	Change to the location where the repo is located on the PC, in the robot, or in the virtual machine or similar and go to the folder e.g:
```bash
cd ~/edu_robot/
```
3.	Download the latest code:
```bash
git pull
```
> **_Note:_** If an error message is displayed here due to existing changes, see the chapter "Why GitHub" to find out how to solve this problem. Make sure to save important changes beforehand.
4.	Change to the corresponding Docker folder, e.g:
```bash
cd ~/edu_robot/docker/iot2050/ 
```
5.	Start a new Docker container:
```bash
docker compose up
```
6.	Possibly delete old container (see chapter "Why Docker")

### Example applications
See the linked repositories above for sample codes you can access.
For **beginners** we recommend starting with the PS5 controller.
You should then work through the [NodeRed example](https://github.com/EduArt-Robotik/edu_nodered_ros2_plugin), for example. You can then look at how the "Don't hit the wall" example in NodeRed can also be implemented in c++ or Python. This can be found in our [edu_robot_control_template] (https://github.com/EduArt-Robotik/edu_robot_control_template). You can then create your own code. We recommend either working natively on ROS2 in a virtual machine on your system or creating your own Docker containers on the robot. To do this, copy all the necessary files, e.g. from our [edu_robot repository] (https://github.com/EduArt-Robotik/edu_robot/tree/main/docker/iot2050). However, this is rather expert knowledge.







