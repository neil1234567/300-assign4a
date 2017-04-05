Consider the following problem; there is a ferry dock on each side of a river. We will
call this dock on this side of the river the ferry’s home dock. We will call the dock on the other
side of the river the ferry’s destination dock. The ferry’s destination dock is downstream of the
ferry’s home dock. At the ferry’s home dock vehicles containing passengers load on the ferry to
travel across the river. The ferry cannot leave the ferry’s home dock until a full load of vehicles
have been loaded. At the ferry’s destination dock the vehicles unload from the ferry. The ferry
cannot leave the unloading ferry dock until after all vehicles on the ferry have unloaded. The
ferry needs to return to the ferry’s home dock empty in order to make it upstream successfully.
We need to consider vehicles traveling in one direction only from the ferry’s home dock to the
ferry’s destination dock. All following conditions must be satisfied.
a) A vehicle is either a truck or a car. A vehicle is represented by a process.
b) The captain is represented by a process
c) Different waiting lines at the ferry dock should be represented in your program as different
message queues. Message queues may hold messages from vehicles to the captain and
messages from the captain to the vehicle or vehicles. You will need more than one message
queue
d) Vehicles arrive at the home ferry dock at random times. In particular the time between the
arrivals of two successive vehicles is taken from a uniform random distribution.
A. The maximum length of time between the arrivals of two vehicles should be
specified by the user of the program.
e) The user should specify the probability that the next vehicle to arrive will be a truck.
f) When a vehicle arrives at the ferry dock it sends a message to the captain indicating it is
now waiting for the ferry
g) The ferry can take six cars (or equivalent) across the river each trip. One truck takes the
same space on the ferry’s deck as two cars.
h) On average trucks are heavier than two cars so the Ferry can carry a maximum of 2 trucks.
i) The ferry only makes a trip from the home dock to the destination dock when it is fully
loaded (six cars, two trucks and two cars, one truck and four cars).
j) When the ferry arrives the home dock (or is ready to load for its first trip of the day) the
captain will signal that the ferry is about to load
k) All vehicles presently in line when the captain signals that the ferry is about to load will be
considered to be waiting vehicles.
l) Any vehicle not already in line when the captain signals the ferry is about to load will be told
to wait in a separate lane (queue). Call any such vehicle a late arrival
m) To begin loading at the ferry’s home dock the captain will signal enough vehicles for a full
load. The following rules should be followed when determining which vehicles the captain
should signal (which vehicles to load):
A. Signal the first two waiting trucks. Here the first truck is the truck that arrived at the
home ferry dock first (earliest).
i. If there are less than three trucks waiting signal all waiting trucks,
B. Signal enough waiting cars to fill the ferry.
C. If there are not enough waiting cars to fill the ferry then consider the vehicles that
are late arrivals
i. If there is one or more trucks among the late arrivals, and there is room on
the ferry for a truck or trucks, then signal the late arrival truck or trucks to
load
ii. If there are no trucks (or the ferry is not full after trucks that fit have been
loaded) then signal the late arrival cars and trucks to join the end of the
waiting line
D. If there are presently no late arrivals that fit on the ferry, and the ferry is not yet full
load each vehicle that fits on the ferry as it arrives, until the ferry is full.
E. If the ferry is fully loaded then the vehicles in the late queue should be signalled to
move to the end of the lo
n) The ferry cannot leave until a full load of vehicles has been loaded (both the captain and the
vehicles themselves must know that they have been loaded. that is they must have receive
and processed messages).
A. The vehicles the captain signalled in m) will load onto the ferry.
B. When a vehicle is loaded onto the ferry it will signal the captain that it has
completed loading
C. When the captain knows all vehicles are loaded, the captain will tell vehicles that the
ferry is about to sail
D. The ferry can sail
When the ferry arrives at the unloading ferry dock the vehicles will be told to unload by the
captain, as they unload they should signal the captain that they have unloaded. When all
vehicles have unloaded the ferry returns to the loading ferry dock for the next load.
Your ferry simulation should end when the ferry arrives at the loading ferry dock for the
11
th
load. 
