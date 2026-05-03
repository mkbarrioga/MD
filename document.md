# SACA Study Guide: Electrical Systems (C-201) and Sensor Logic Systems (C-205)

> **🟡 LEGEND — How to read this guide**
> Throughout this document, content marked with the 🟡 symbol or wrapped in a yellow callout block corresponds to material that was highlighted in **yellow text** on the original lecture slides.


# PART ONE — Electrical Systems (C-201)

## Module 1: Basic Electrical Circuits

### What electricity actually is

Electricity is the flow of electrons through a conductor. Electrons are the negatively charged particles in an atom, and when they move through a wire they carry energy from one place to another. That moving stream of electrons is what we call current, and current is the thing that does the actual work in any electrical system, whether it is lighting a bulb, turning a motor, or pulling in a relay coil.

There are two fundamentally different ways current can flow, and the distinction between them shows up everywhere in this course. Direct current, abbreviated DC, flows in only one direction — the electrons leave the positive terminal of a power supply, travel through the circuit, and return to the negative terminal in a steady, one-way stream. Alternating current, or AC, reverses direction many times per second; in the United States it cycles 60 times per second, which we describe as 60 Hz. Most of the electrical power generated in the world is AC because AC is much easier to transmit over long distances and can be readily converted to DC when a device needs it. 🟡 Common DC sources include batteries and DC power supplies (which are themselves devices that convert AC into DC).

### The four basic components every circuit needs

Every electrical circuit, no matter how simple or complex, is built from the same four basic building blocks. The **power supply** is the source of electrical energy — it provides both the high-potential terminal and the low-potential terminal that drive current through the circuit. The **input device** controls the flow of current; the most common input device you will encounter is a switch, but later modules will introduce sensors and relays that act as input devices too. The **output device**, also called the **load**, is the component that actually consumes electrical energy and does useful work; lamps, motors, solenoids, and buzzers are all examples. The **conductor** ties everything together — it is simply the wire (almost always copper) that lets current flow between the other components.

A circuit is described as **closed** when there is a complete, unbroken path for current to flow from the power supply, through the loads, and back to the power supply. It is **open** when that path is broken anywhere along the way. A switch is just a deliberate, controllable break in the circuit: when the switch is closed the circuit is closed and current flows, and when the switch is open the circuit is open and current stops.

### Switches — operators and contacts

Every switch has two functional pieces. The **operator** is whatever causes the switch to activate — your finger pressing a button, a knob being turned, a machine part bumping into a lever, a magnetic field appearing nearby, or an electrical signal energizing a coil. The **contacts** are the metal pieces inside the switch that actually open and close to make or break the circuit.

Contacts come in two normal states. **Normally Open (N.O.)** contacts are open until something acts on the operator, at which point they close. 🟡 **Normally Closed (N.C.)** contacts are closed until the operator activates, at which point they open. The word "normal" here means the unoperated, unenergized, resting state — it is the state the switch sits in when nothing is happening to it.

Switch operators fall into two broad categories. **Manually operated** switches are activated by a person; the three common kinds are knife switches (which give visual confirmation of the switch's state and are often used as main disconnects), pushbutton switches (which are usually momentary and are commonly used for start and stop functions), and selector switches (which are often used to choose between machine modes). **Automatically operated** switches are activated by a sensor, by a part of the machine itself, or by some other device — limit switches, relays, and electronic sensors all fall into this category, and they are the main subject of the second half of this guide.

### The five output devices

There are five output devices you should be able to recognize. A **lamp** gives off light when current passes through its resistive element. A **resistor** limits the flow of current. A **buzzer** produces sound. A **solenoid** has a coil that, when energized, pulls an internal armature in a straight line — solenoids are how we produce linear mechanical motion electrically, and they are central to how electrically controlled valves work. A **motor** converts electricity into rotary mechanical motion: when current flows through it, a magnetic field is set up that causes a shaft inside the motor to rotate.

### How circuits get drawn

Pictorial diagrams use realistic pictures of the components, which is fine for very simple circuits but becomes unreadable as soon as the circuit gets complicated. 🟡 Electrical schematic diagrams use standard symbols instead, and they do not try to show physical placement — they show how components are electrically connected. Most schematics also label the electrical parameters of interest, such as the voltage at various points, the current through various branches, and the resistance of various components.

---

## Module 2: Electrical Measurements

### Series and parallel — the two ways to connect things

Every electrical circuit is built from a combination of two basic connection patterns. 🟡  In a **series** circuit, there is exactly one path for current to flow, and the total current flows through every component in turn. In a **parallel** circuit, there are two or more paths for current to flow; the current splits at one node, travels through the parallel branches, and rejoins at another node further down. This split-and-rejoin behavior is the defining feature of parallel.

> **🟡 OHM'S LAW — KEY EMPHASIS**
> Voltage equals current times resistance: **V = I × R**. This single relationship can be rearranged two other ways: **R = V / I** and **I = V / R**. Power is then **P = V × I**. As a worked example, if the current is 0.3 amps and the resistance is 100 ohms, then the voltage is 0.3 × 100 = 30 volts. As another example, if the current is 0.2 amps and the total resistance is 40 ohms, then the voltage is 0.2 × 40 = 8 volts. Memorize this triangle of relationships — it is the single most-used formula in this entire course.

### Voltage — the force that pushes current

**Voltage** is the force that causes electrons to move through a circuit. 🟡 Another name for it is electromotive force, which is why it is sometimes represented by the letter E, though in schematics you will more often see it written as V. Voltage is measured between two points — it is fundamentally a difference in potential between one place and another. When the source produces direct current we describe the voltage as DC (for example, 12 VDC), and when the source produces alternating current we describe the voltage as AC (for example, 12 VAC). When you see a voltage written with just V and no AC or DC qualifier, it is understood to mean DC.

To measure voltage, you connect the leads of your meter **across** the component you are interested in — that is, in parallel with it. You can think of this in terms of three points along a circuit. Point A, closest to the high-potential terminal of the supply, has the highest potential. Point C, closest to the low-potential terminal, has the lowest. Point B sits somewhere in between because there is a resistor on each side of it.

In a **series circuit**, the total voltage from the power supply is divided up among the loads. Each load uses some portion of the voltage, leaving less for the next load down the line. The amount each load uses is called its **voltage drop**, and the size of that drop depends on the resistance of that particular load. In a **parallel circuit**, by contrast, the same voltage is available to every branch — every branch sees the full source voltage, and the voltage drop across each branch is identical.

### Current — the flow itself 🟡 

**Current** is the actual flow of electrons through the circuit, and it is measured in amperes (amps), abbreviated A. When values are very small, we use milliamps (mA), where one milliamp is one-thousandth of an amp.

🟡 To measure current, you must place the ammeter **in series** with the component, which is different from how you measure voltage or resistance. This is because the current you want to measure has to actually flow through the meter for the meter to count it.

In a **series circuit**, the current is the same everywhere — it does not change as it flows through the loads. This is why it is uncommon to connect output devices in series: if one of them fails open, current stops flowing and every load loses power. (Older holiday lights worked this way, which is why a single burnt-out bulb would kill the whole string.) Note, however, that it is very common to connect *input* devices in series, because that is how AND logic gets built. In a **parallel circuit**, the current divides among the branches; how much goes through each branch depends on that branch's resistance. If one branch fails, the others keep working — which is why newer holiday lights and almost all residential and commercial wiring use parallel connections.

### Resistance — opposition to current flow

🟡 **Resistance** measures how much a component opposes the flow of current. The unit is the ohm, abbreviated with the Greek letter Ω. Higher values get expressed in kilo-ohms (kΩ, thousands of ohms) or mega-ohms (MΩ, millions of ohms).

You measure resistance with an ohmmeter, placing the test leads in parallel with the component. Critically, you must turn off the power to the circuit and disconnect at least one terminal of the component before measuring, because the ohmmeter sends its own small test current through the component and outside power would corrupt the reading or damage the meter.

🟡 When resistors are connected in **series**, their individual resistances simply add together to produce the total. When resistors are connected in **parallel**, the total resistance actually decreases as you add more resistors, because each new branch you add gives the current another path. A useful mental model is the toll-booth analogy: a single toll booth slows cars down, three toll booths in series slow them down even more, but three toll booths in parallel actually speed traffic up because each car has more lanes to choose from.

### Continuity — is the path complete?

🟡 **Continuity** simply means there is a continuous, complete path for current to flow. Wires must have continuity or the circuit will not operate. There are two ways to test for it. You can measure resistance with an ohmmeter — if the conductor has continuity, the display will show a very small value (around 0.01 Ω), and if there is an open in the conductor, the display will show an out-of-range indication. Alternatively, you can use a continuity tester, which is a small device with a power source and a sounding device built in; it indicates continuity by buzzing when the test leads are placed across a path that is intact.

---

## Module 3: Circuit Analysis

### Total resistance in series and parallel

🟡 In a series circuit, total resistance is the simple sum of the individual resistances — add them all up and you have the total. In a parallel circuit, the total resistance decreases as you add more resistors. The formula uses reciprocals: 1 divided by the total resistance equals the sum of 1 divided by each individual resistance. As an example to work through, if you have 60-ohm, 45-ohm, and 35-ohm resistors connected in parallel, the total resistance comes out lower than the smallest individual resistor (35 ohms) because each additional parallel path makes it easier overall for current to flow.

### How resistance and current relate

🟡 Current in any circuit, series or parallel, responds to changes in resistance. An increase in resistance causes a decrease in current, and a decrease in resistance causes an increase in current. This is just Ohm's law expressed in plain language: since I equals V over R, when R goes up and V stays the same, I must come down.

### Ohm's law and Kirchhoff's laws

> **🟡 Ohm's Law — the unifying relationship**
> Voltage, current, and resistance are tied together by Ohm's law, which applies to any circuit where the loads are purely resistive. The plain-English statement is that one volt can push one amp through one ohm of resistance. With Ohm's law, if you know any two of the three quantities you can calculate the third.

**Kirchhoff's Voltage Law** says that in a series circuit, the total voltage from the source equals the sum of the individual voltage drops around the loop. Every volt that the source supplies has to get used up somewhere by the loads. **Kirchhoff's Current Law** says that the amount of current flowing out of the power supply equals the amount flowing back to it. In a parallel circuit, the total current to and from the supply is called the **main line current**, and it equals the sum of the currents through each parallel branch.

### Power

🟡 **Power** measures the energy consumed by a circuit, and it is measured in watts (W). The defining statement is that one watt is consumed when one volt pushes one amp through a circuit, which gives the formula **Power = Current × Voltage**, or P = I × V.

### Circuit protection — fuses and breakers

High current can damage components, and there are two main reasons it might occur: too many loads connected to a circuit (overload), or a short circuit, which is a direct path with little or no resistance. Two devices protect against this. A **fuse** is a low-cost protection device placed in series with the circuit; it consists of a conductive wire or metal foil strip inside a glass tube, and when the current exceeds the fuse's rating the wire melts and opens the circuit. 🟡 A good fuse has continuity; a blown fuse does not. Fuses are best used where problems rarely occur, such as a car's lighting system, because they have to be replaced after every fault.

A **circuit breaker** does the same protective job but can be reset instead of replaced. There are two kinds. 🟡 A **thermally triggered** breaker trips because of heat caused by excessive current, and it has a built-in lag time before tripping because temperature has to rise. A **magnetically triggered** breaker trips because of the strength of the magnetic field created by excessive current, and it trips immediately on a current surge but might not respond to a slow gradual increase. A **thermomagnetic** breaker combines both mechanisms and is the most common type in everyday use.

---

## Module 5: Combination Circuits

### Series-parallel circuits

A **series-parallel** circuit, also called a combination circuit, contains both series and parallel elements. The trick to working with these is to remember the two defining properties: components connected in series share the same current, and components connected in parallel share the same voltage. To identify which sections are which, you trace the current path looking for nodes where the current splits (the start of a parallel section) and nodes where the current recombines (the end of a parallel section).

To analyze a combination circuit, the general approach is to simplify it down to a pure series circuit by replacing each parallel section with its equivalent resistance, then use that simplified picture to find the total resistance, then use Ohm's law to find the total current, and finally work backward through the original circuit to find the voltage drops and branch currents.

### Variable resistors — rheostats and potentiometers

A **variable resistor** is a resistor whose value can be adjusted by hand. It can have either two or three terminals: the two outside terminals act like a fixed resistor, and the center terminal is connected to a slider, called a wiper, that is moved by a knob.🟡 The two main types are the **rheostat**, used primarily in high-power circuits, and the **potentiometer**, used primarily in low-power electronic circuits.

### Voltage dividers

A **voltage divider** is a circuit that creates an output voltage lower than the source voltage. It consists of two or more resistors in series with the source; the voltage at the midpoint is some value between the source voltage and zero, determined by how the resistors split things up.

When you design a voltage divider, three considerations matter: how constant the load voltage needs to be, how much power the circuit will consume, and whether the load resistance is high or low. Three common designs result.🟡 A **firm voltage divider** uses a bleeder resistor that is one-tenth the resistance of the load — it does not produce a perfectly constant load voltage but does not waste much power either. A **stiff voltage divider** uses a bleeder resistor only one-hundredth the resistance of the load — it gives a much more constant output voltage but wastes ten to a hundred times the power that the load itself consumes. A **loaded voltage divider** is used when the load resistance is relatively low; the bleeder resistor is ten times the load resistance, and the power wasted is only about ten percent.

A **bleeder resistor**, in this context, is a resistor connected in parallel with a capacitor (or across the output of a power supply) whose job is to discharge stored energy after the circuit is powered off, so that voltage does not linger dangerously on capacitors after shutdown.

### Shorts and opens — the two basic faults

A **short circuit in series** may or may not cause excessive current. If a single component in the chain is shorted, current keeps flowing through the rest of the circuit; only the shorted component is bypassed, which means the current rises a bit because total resistance dropped. A **short circuit in parallel** is much more dramatic — it shorts out the entire circuit because all the current diverts through the shorted branch and bypasses all the other branches. Because the shorted branch has practically no resistance, the current spikes, and a short across the power supply can damage or destroy it.

To troubleshoot a short, the four-step procedure is: first, look for visible signs of damage; second, disconnect the power supply; third, connect an ohmmeter across the main line; fourth, disconnect each branch one at a time and watch the resistance reading. If the resistance stays close to zero when you remove a branch, the short is in another branch. If the resistance suddenly rises when you disconnect a particular branch, that is the shorted one. If disconnecting all branches still gives you a zero-ohm reading, the short is in the main line itself.

An **open circuit** is the opposite — somewhere a connection has broken. Many opens are actually caused by shorts, because a short that continues for any length of time can burn a wire or component until it opens, or it can blow a fuse or trip a breaker (which is itself an open).🟡 If one branch of a parallel circuit opens, the rest of the circuit keeps operating but with reduced total current, because the effective resistance has gone up. If an open occurs in a series circuit, current cannot flow at all.

To find an open, the procedure is: disconnect the power supply, connect an ohmmeter across the main line, and then disconnect each branch one at a time. The total resistance should rise as each branch is removed; if disconnecting a branch has no effect on the total resistance, that branch must already be open. More than one branch may have an open, so keep checking after you find the first one. If the open is in the main line, the circuit will not operate at all.

---

## Module 6: Transformers

### What a transformer does

🟡 A **transformer** is an electrical device that converts AC electricity from one voltage level to another. Transformers are how the power company takes the very high voltages used for long-distance transmission and steps them down to the lower voltages we can safely use in homes and factories, and they are also used inside the power supplies of many devices like computers.

🟡 A transformer has three basic components. The **primary coil** receives the input voltage, the **secondary coil** delivers the output voltage, and the **core** conducts the magnetic field between them. The principle behind it is **mutual inductance**: AC current flowing in the primary coil creates a changing magnetic field in the core, which in turn induces an AC voltage in the secondary coil. A transformer cannot work with DC — it requires the changing magnetic field that only AC produces.

### Turns ratio and voltage relationship

To determine the output voltage you need only two pieces of information: the input voltage and the **turns ratio**, which is the ratio of the number of turns of wire on the primary coil to the number of turns on the secondary coil. The output voltage is the input voltage divided by the turns ratio (for a step-down transformer with more turns on the primary than the secondary).

Importantly, input power and output power in a transformer are equal (ignoring small losses). This means there is a tradeoff between voltage and current: when the voltage goes up across the transformer, the current goes down by the same factor, and vice versa. Stepping voltage down also steps current up.

### Troubleshooting transformers

When a transformer fails, the failure shows up as either a short or an open in one of the coils. Two methods catch most problems. First, you can simply measure the input and output voltages — if the input is normal but the output is wrong or absent, the transformer is the suspect. Second, you can check it with an ohmmeter, looking for several specific failures. **Opens in coils** show up as infinite resistance across a winding that should have continuity. **Shorts between the primary and secondary coils** show up as resistance between the primary and secondary, when the reading should be infinite (the two coils should be electrically isolated from each other). **Shorts within a coil** effectively reduce the number of turns and produce a wrong voltage. **Coils shorted to the core** show up when there is resistance between either coil and the iron core, when the reading should again be infinite.

### Sizing a transformer

🟡 To size a transformer for a particular application, you need to know the available input voltage, the desired output voltage, and the required output current — both **in-rush** current (the surge that happens at startup) and **steady-state** current (the normal operating current). Specification sheets list a rating known as the **steady-state Volt-Amperes (VA)** rating. The rule is to select a VA rating that is above the required value but as close to it as possible. Never undersize a transformer. 🟡 For machines with motors or other devices that have high in-rush currents, the in-rush is the critical value to consider when sizing — if you only sized for the steady-state load you would trip protection or stress the transformer every time the machine started.

The current load drawn by the primary winding is the current that has to be supplied to the primary in order to power the load on the secondary. Use this primary current value to size the upstream circuit breaker that will protect the transformer.

### Categories of transformers

Most transformers fall into two categories. **Isolation transformers** have primary and secondary windings that are physically and electrically separated; they are coupled magnetically rather than electrically, which means voltage spikes on the primary are greatly reduced before they reach the secondary. Some isolation transformers actually produce an output voltage equal to the primary voltage — they exist purely for the isolation, not for changing the voltage. **Autotransformers** use only a single coil that serves as both primary and secondary; connections at intermediate points along the coil, called **taps**, are used to produce different ratios and output voltages.

🟡 A **control transformer** is a transformer that reduces voltage from the main power line down to a lower voltage that runs a machine's electrical control system. The most common type has two primary coils and one secondary coil, and in most cases it reduces 240 VAC or 480 VAC down to 120 VAC. Metal links connect the primary coils together; 🟡 if the supplied line voltage is 240 VAC, the primaries are connected in **parallel**, giving a 2:1 turns ratio. 🟡 If the supplied line voltage is 480 VAC, the primaries are connected in **series**, giving a 4:1 turns ratio.

A **tap** is simply a connection at some point between the ends of a coil, allowing a different output voltage to be drawn from that point. 🟡 A **center tap** is a tap that splits a secondary winding exactly in half. A common application is a distribution transformer used by homes and businesses to provide both 240 VAC and 120 VAC from a single transformer; in that arrangement, the center tap is connected to earth ground and becomes the common conductor.

---

# PART TWO — Sensor Logic Systems (C-205)

## Module 1: Control Logic

### Manual switches — the SPST baseline

> **🟡 SPST — the most common switch type**
> SPST stands for Single Pole, Single Throw. SPST switches are the most common type, and they have only two wires. Most pushbuttons and limit switches are SPST devices. There are also SPDT (single pole, double throw), DPST (double pole, single throw), and DPDT (double pole, double throw) switches, with single-break or double-break variants of each, but the SPST is the foundation.

Pushbuttons are typically SPST or SPDT. Two-position selector switches are typically SPDT, and so are most limit switches. Multi-position relay switches and some heavy-duty pushbuttons can be DPDT, with two independent contacts that move together.

### Solid state switches — transistors as switches

The most common switch in the entire world is the transistor — your phone or computer contains hundreds of billions or even over a trillion of them. A transistor is **solid-state**, which means it has no moving parts at all, unlike a limit switch or a pushbutton.

> **🟡 Used in control circuits, a Transistor is just an SPST switch — either on or off!**
> When you see a transistor in a control circuit, do not be intimidated by the symbol. For circuit-analysis purposes you can treat it exactly like a single-pole, single-throw switch that is either on or off. Solid state relays and electronic sensors all use transistors as their switching elements, which is what makes them so much faster than mechanical alternatives.

### Switch states — normal, operated, NO and NC

Every contact within any switch has a **normal state**, defined as the state of the switch when it is unoperated and unenergized. A **Normally Open (NO)** contact is open in its normal state and closes when something operates the switch. A **Normally Closed (NC)** contact is the reverse — closed in its normal state and opens when operated. Switches with multiple contacts can have any combination of NO and NC contacts, which is what makes complex relays so versatile.

A **selector switch** is built around a conducting wafer that rotates with a knob. A different circuit can be connected to each terminal or position. In a three-position selector, the center position typically does not operate any contacts — it is the "off" or "neutral" mode. In a two-position selector, the solid arrow on the schematic symbol shows the unoperated state.

### Control logic — the six logic elements

> **🟡 Control logic is a way of connecting switches to make decisions that control a machine's operation. There are six main arrangements of switches that are used for control. Hand switches, relays, limit switches, and solid-state switches all make up these logic elements.**

The six elements are AND, OR, NOT, NAND, NOR, and Memory. Each one is built from a particular arrangement of NO or NC contacts.

> **🟡 The three basic logic shapes**
> **AND** logic requires two switches in series to be closed. Both must be closed before the output energizes. **OR** logic requires one of two switches in parallel to be closed. Either one closing is enough. **NOT** logic requires one normally closed switch to be open — it inverts whatever signal is fed into it.

> **🟡 The compound logic shapes**
> **NAND** logic requires two or more normally closed switches arranged in parallel. **NOR** logic requires one or more normally closed switches in series, all of which have to be open for the output to energize. 🟡 **Memory logic** is used to keep an output energized even after the input signal that turned it on is removed; it is also known as a **seal-in circuit**, and you will see it in almost every industrial control diagram.

> **🟡 Common applications of each logic type**
> **AND** is commonly used for two-hand start circuits — both buttons must be pressed before the machine starts, which keeps both of the operator's hands away from the danger zone. **OR** is commonly used for remote-start pushbuttons — pressing either one starts the machine. **NOT** is commonly used for emergency stop pushbuttons — the eStop is normally closed in its rest state, so opening it (pressing the button) interrupts the circuit. **NAND** is commonly used for multiple stop pushbuttons — pressing any one of several stop buttons will halt the machine. **NOR** is commonly used for multiple stop pushbuttons in some configurations as well.

### Ladder diagrams — the main schematic style for industrial controls

A control circuit drawn with logic elements like PLCs or other control logic components is called a **ladder diagram**, also called ladder logic. It is named that way because the two vertical lines on the sides (the power rails, labeled L1 on the left and L2 on the right) and the horizontal "rungs" between them visually resemble a ladder. Ladder diagrams show only the control and power devices; the actual wiring to motors and other actuators is shown on a separate **power diagram**.

> **🟡 Ladder Diagram Rules**
> Ladder diagrams show only four types of components: power supply, input devices, output devices, and conductors. All components must be labeled. All conductors must be numbered. All rungs must be numbered. Only control devices are shown — power devices are on the power diagram. Only one load is allowed per rung. The diagram is read left to right and then top to bottom. Inputs are always on the left side of each rung, and outputs are always on the right side.

> **🟡 Reading or "following" a ladder diagram**
> Start at the first rung. Read left to right. Move to the next rung. Read left to right. Repeat until the last rung. The pattern is always **left to right and then top down** — the same way you would read a page of English text.

A **power diagram** accompanies the ladder diagram and shows the overall electrical-system connections to motors and other actuators — the contacts of a motor starter, the thermal overload heaters, the wiring to a three-phase motor, the connections from a directional control valve to its cylinders, and so on. Whenever a control circuit operates a power device, a power diagram should accompany the ladder diagram so you can see how the controlled device is actually wired.

---

## Module 2: Valves and Relays

### Directional Control Valves (DCVs)

A **DCV — Directional Control Valve** — controls the flow of air (in pneumatic systems) or fluid (in hydraulic systems) by routing it to different ports, which are pressurized lines connected to actuators like cylinders. DCVs can be operated in four common ways: by hand (manual), by an electric solenoid, by a pneumatic or hydraulic pilot signal, or by a cam (similar to a limit switch).

The internal mechanism that does the routing is called the **spool**. The spool is a precisely machined sliding piece inside the valve **body** that, depending on its position, either blocks or connects various **ports**. Solenoids energize coils that move the spool back and forth electromagnetically. A manual DCV uses a lever physically linked to the spool. Pneumatic-pilot DCVs use a pressurized pilot air signal to push the spool. Not all DCVs use spools — some use poppets, rotary disks, or other mechanisms — but spool valves are the most common type you will encounter.

In a typical solenoid-operated DCV with two solenoids, the **unoperated** state has both solenoids unenergized and the spool in the center position, with no flow to either output port. When **Solenoid A** is energized, the spool slides one way and connects port A to pressure (P) and port B to exhaust (S), which extends a connected cylinder. When **Solenoid B** is energized instead, the spool slides the other way and connects port A to exhaust (R) and port B to pressure (P), which retracts the cylinder.

### The solenoid manual-override trick

Solenoid-operated pneumatic valves have **manual overrides** — small actuators built into the valve that let you mechanically push the spool without energizing the solenoid. These are extremely useful for troubleshooting, because the technician can activate the valve without operating any switch and even without electrical power being present at all. A ball-point pen or a small Phillips screwdriver is commonly used to push the override button.

### Relays — electrically operated switches

**Relays** are electrically operated switches whose contacts open and close in response to electrical signals coming from somewhere else in the system. Compared to pushbuttons and other manual switches, relays are usually heavier-duty: they can carry higher currents and they can withstand more on-off cycles before wearing out.

Relays come in two construction types depending on how the switching is actually done. Relays that use mechanical contacts and a magnetic coil to move them are called **electromechanical relays (EMRs)**. Relays that use transistors instead of mechanical contacts are called **solid-state relays (SSRs)**.

Within the EMR family, two physical styles are common. A **general-purpose relay** is low-cost, light-duty, and often has a transparent housing so you can see the contacts move; some are plug-in for easy replacement. A **machine control relay** is heavier-duty, designed for long operating periods, and is the standard for industrial use. Internally, an EMR is built around a **solenoid coil** that, when energized, pulls a moving armature against a spring. The armature carries one or more sets of **contacts**, which can be either NO or NC, and the contacts open or close as the armature moves.

A relay shows up on a ladder diagram in two separate places. The **coil** is shown as a circle on the right side of the diagram, drawn like an output device because that is what it electrically is — it is energized by the control circuit. The **contacts** of the same relay appear elsewhere in the diagram, on the left side of various rungs, drawn as switches that act as input devices. 🟡 A coil labeled 1CR will have contacts labeled 1CRA, 1CRB, and so on, with one letter per contact. Showing the coil and contacts on different rungs of the same diagram is called **detached symbology**, and it is the standard convention for ladder diagrams.

### Control relay as a memory circuit (the seal-in)

> **🟡 The Memory or Seal-In Circuit**
> The seal-in circuit is one of the most common patterns in all of ladder logic, and you will see variations of it in nearly every industrial machine. It is used whenever you need to keep an output energized after the input signal that turned it on is removed.
>
> Here is how it works. 🟡 When the **Start 1PB** is pressed momentarily, the relay coil **1CR** is energized. Energizing 1CR closes its **1CRA** contact, which is wired in parallel with the start button. When you release the start button, current can still flow to 1CR through the now-closed 1CRA contact, so 1CR stays energized. A momentary press of 1PB therefore keeps 1CR energized **permanently**. The circuit is killed by pressing **Stop 2PB**, which is wired as a normally closed contact in series with everything else; opening it for an instant breaks the seal-in path, 1CR drops out, 1CRA opens, and the circuit can no longer hold itself on. The stop button is also commonly called the **eStop**.

### Solid-state relays in detail

A solid-state relay is selected based on a number of factors: mounting type, AC versus DC operation, output voltage, input voltage, output current, and input current. SSRs have several advantages over electromechanical relays — they provide input isolation (often using an internal LED and photodetector pair to optically isolate the control side from the load side, which protects sensitive electronics from the high voltages on the load side), they switch much faster, they have no moving parts to wear out, and they produce no contact arcing.

> **🟡 SSRs are specified for AC OR DC — they are not interchangeable.** A DC SSR cannot be substituted for an AC SSR or vice versa. This is one of the most important things to remember when ordering or replacing one.

Testing an SSR usually comes down to a few voltage checks. First, is the line voltage that supplies the load good? Second, is the control voltage — the signal that is supposed to cause the SSR's output to change — good? Third, when the control voltage is applied to the SSR, does the output actually change state? 🟡 **If the output is zero when it should be present, the SSR has failed.**

When you check the line voltage that supplies the load, you measure between the load wire and ground (or the other side of the AC line, depending on the circuit). If you read no voltage or a very low voltage there, the problem is upstream of the SSR — it is not the SSR itself. When you check the control voltage, measure both before and after the input switch, because switches are always a source of problems; if you have voltage at the supply but not at the SSR input when the switch is closed, the switch is bad. Finally, when the control voltage is properly applied to the SSR, you measure across the load again. If the expected voltage does not appear there, the problem is the SSR itself.

---

## Module 3: Limit Switches

### What a limit switch is and why we use them

A **limit switch** is an input device that automatically opens or closes its contacts based on the position of another part of the machine or the product being worked on. They are simple, low-cost, reliable, and extremely common in industrial machines. Their two main components are the **actuating mechanism** — a lever, roller, plunger, or whisker that gets physically pushed by the moving part — and the **contacts** that open or close when the actuator moves.

### Limit switch states and symbols

Limit switches can be normally open or normally closed and can have one or two contacts. On a ladder diagram, they are always shown in their **unoperated** state — the way they sit when nothing is pushing on the actuator.

> **🟡 Two additional limit-switch states for special cases**
> Occasionally, a limit switch is shown in its operated state because something — a cylinder, a cam, a part — is holding it there at rest. To represent this, two additional symbols are used: **NOHC (Normally Open, Held Closed)** and **NCHO (Normally Closed, Held Open)**. These symbols tell you that the switch is currently being held in the opposite of its normal position by some physical condition.

### Reading ladder diagrams that include limit switches

Limit switches give you the ability to read ladder diagrams that describe sequences of mechanical actions. 🟡 A typical sequencing example works like this: when 1PB is pressed, cylinder 1 begins to extend because 1-SOL is energized. When the cylinder reaches full extension, it physically operates 2LS, which then energizes 2-SOL. An energized 2-SOL causes cylinder 2 to extend; if 2LS opens for any reason, cylinder 2 retracts.

A machine may need to pause or stop between steps. This is most simply done by placing a normally closed limit switch in series with a seal-in to break the seal automatically when the machine reaches a certain position. In a single-cycle reciprocation circuit, the sequence is: pressing start energizes 1CR, which turns on 1-SOL and extends a cylinder; the cylinder eventually trips a limit switch that opens, breaking the seal-in; 1CR drops out and the cylinder retracts. The machine cycles once and stops.

A **continuous-cycle reciprocation circuit** is similar but uses additional relays and limit switches so that the cylinder reciprocates back and forth indefinitely after the operator presses the start button just once. The circuit only stops when the stop pushbutton is pressed.

A **safety interlock** is a particularly important application of limit switches. Machine guards are typically pressed against a limit switch when they are in place. If the guard is removed, the limit switch opens, which kills power to the machine. The purpose is to ensure the guard is in place before the machine can operate, protecting the operator from rotating or moving parts.

---

## Module 4: Timers

### Time-delay relays

Some machines use time itself to control the sequence of events, and the typical device for this is the **time-delay relay**. A time-delay relay changes the state of its contacts after a predetermined time has elapsed. It has three components: a **coil**, which when energized causes the contacts to change state (eventually); one or more sets of **contacts** that include both NO and NC types; and a **timing mechanism** that determines the desired delay.

A time-delay relay operates in one of two ways: **on-delay** or **off-delay**. The two have different schematic symbols and very different behaviors.

### On-delay timers

In an **on-delay** timer, when the coil is energized the relay's timing mechanism starts running, but the contacts stay in their normal state during the timing period. Once the preset time delay is reached, the contacts move to their energized states. The contacts remain in those energized states until the coil is de-energized, at which point they snap immediately back to normal. The two on-delay contact symbols are **NOTC (Normally Open, Timed Closed)** — closes after the delay — and **NCTO (Normally Closed, Timed Open)** — opens after the delay.


### Off-delay timers

In an **off-delay** timer, the behavior is mirrored. When the coil is energized, the contacts move immediately to their energized states, but the timing mechanism does not start running yet. Once the coil is de-energized, the timer starts running, and the contacts stay held in their energized states during the timing period. Once the preset time is reached, the contacts return to their normal states. The two off-delay contact symbols are **NOTO (Normally Open, Timed Open)** and **NCTC (Normally Closed, Timed Closed)**.


### Time-driven sequencing

> **🟡 Time-driven sequencing uses timers to sequence the operation of machines.**

A common example is a circuit that starts three motors but staggers them so they do not all draw their startup current simultaneously. Pressing the start pushbutton starts motor M1, energizes timer 1TR, and seals in both. After the time delay set on 1TR, the on-delay contact on 1TR closes and starts motor M2 along with timer 2TR. After the time delay set on 2TR, the on-delay contact on 2TR closes and starts motor M3.

> **🟡 A few additional yellow-emphasis facts about timers**
> **Solid-state** time-delay relays use a resistor-capacitor network as their timing circuit (the time it takes the capacitor to charge through the resistor sets the delay). **For each distinct operation in a time-driven sequence, a timer must be assigned.** To avoid overheating a motor and causing damage, it is recommended that the motor be **unloaded** when it is started — an example of an unloaded start of a motor is a centrifugal air **compressor**.

---

## Module 5: Advanced Systems

### Multiple cylinders in a machine

Machines often use multiple cylinders that need to work in synchronization. When two cylinders need to work in parallel because of design or space considerations, the easiest mechanical solution is to attach them both to the same machine part so they have to move together. For any other arrangement where the cylinders need coordinated but not identical motion, **flow control valves** and **limit switches** are used to synchronize them.

### Simple multiple-limit-switch circuits

> **🟡 Normally a cylinder will retract when it extends fully and hits its limit switch.**

Here is how a clamping circuit using two cylinders works in detail. The key element is the normally-closed contact of relay 2CRA in the start rung. When 1PB is pressed, 2CRA is closed (because 2CR is currently unenergized), so 1CR energizes and the solenoid shifts to extend both cylinders in parallel. One cylinder may operate its limit switch first, but **both** limit switches must be operated before 2CR can energize. When 2CR finally does energize, it de-energizes 1CR through its NC contact, the solenoid shifts back, and both cylinders retract.

### Two modes of operation: automatic and jog

Most industrial circuits offer two operating modes that an operator can select between. **Automatic mode** runs the machine continuously after a single momentary press of the start pushbutton — the seal-in keeps the relay energized until something stops the cycle. **Jog mode** (also called manual mode) is different: the solenoid only energizes while the start pushbutton is being held. When the operator releases the button, the cylinder stops moving immediately. Jog mode is useful for setup, troubleshooting, and clearing jams.

### Guidelines for working with manual controls

Several rules of thumb apply when designing or working with manual controls. Solenoids should only be energized through relays — never wire a solenoid directly to a manual switch. Manual overrides on solenoid valves should not be used during normal operation, only for troubleshooting. Jogging should be done at slow speeds. Mode lockouts should be used to make sure the machine cannot be put into jog mode while it is running automatically, or vice versa. And only pushbuttons (not maintained switches like selectors) should be used to jog, so that releasing your finger always stops motion.

---

## Module 6: Introduction to Electronic Sensors

### Why electronic sensors exist alongside mechanical limit switches

Electronic sensors offer several capabilities that simple limit switches cannot match.

> **🟡 Advantages of electronic sensors**
> Electronic sensors have **higher operating speed**, which means they can sense faster than a mechanical switch ever could. They make **no physical contact** with the part, which eliminates wear on both the sensor and the part. They have **lower maintenance cost and longer life** because there is nothing to wear out. They can sense not just position but also **material type and color**, which a limit switch could never do. **Two-wire sensors** are normally connected to a terminal on the power supply and to the controller input terminal on the sensor.

> **🟡 Drawbacks of electronic sensors**
> They require a **more complex control system** than simple mechanical switches do. They usually have a **low power (voltage and current) handling capacity**, which means you typically cannot drive a heavy load directly from a sensor — you have to go through a relay. And they require **optical isolation** to protect the control system against electrical noise that the sensor might pick up.

### The five common types of electronic sensors

The five most common types of electronic sensors are the **inductive proximity sensor**, the **capacitive proximity sensor**, the **magnetic reed switch**, the **Hall effect sensor**, and the **photoelectric sensor**.

> **🟡 The major difference between mechanical and electronic sensors (with the exception of the reed switch) is that electronic sensors use transistors as switches and are much faster.**

### Two transistor-switching technologies: PNP (sourcing) and NPN (sinking)

Sensors and other solid-state devices use one of two transistor configurations to switch their outputs. The choice between them affects how the sensor wires into the rest of the circuit.

> **🟡 PNP = Current "Sourcing"**
> A PNP sensor is used in circuits that require a **high signal** (+12V, +24V, etc.) when activated. When the sensor activates, it provides positive voltage to the load. The output transistor connects the load up to the positive supply rail.

> **🟡 NPN = Current "Sinking"**
> An NPN sensor is used in circuits that require a **low signal** (0V) when activated. When the sensor activates, it pulls the output down to ground (0V). The output transistor connects the load down to the negative rail.

> **🟡 The transistors inside these sensors are just solid-state switches!**
> No matter how complex the sensor electronics get, the actual output is still just an electronic on-off switch.

### Note about sensor wiring in the lab

When testing sensors with an LED indicator lamp, remember that LEDs are **polarized**: electricity only flows through them in one direction. The white wire must be connected to plus (+), and the black wire must be connected to common (ground), in order for the LED to operate. If you wire the LED backwards, no light will appear regardless of whether the sensor is working correctly.

### Inductive proximity sensors

An **inductive proximity sensor** uses an AC current flowing through a coil to create a magnetic field at the sensor's head. When metal moves into that field, some of the magnetic energy is absorbed, which the sensor's electronics detect.

The **five things that affect performance** are the target material, the target size, the target distance from the sensor head, the size of the sensor head itself, and the way the sensor is mounted (whether nearby metal interferes with the field).

> **🟡 Inductive sensors can only sense metals. Ferrous metals (steel and iron) are by far the best targets for detection.** Non-ferrous metals like aluminum, copper, and brass can be detected, but at significantly shorter ranges than ferrous metals.

### Capacitive proximity sensors

A **capacitive proximity sensor** uses an AC current flowing to two plates to create an electrostatic field — essentially a small voltage difference — at the sensor head. When any object with sufficient dielectric properties enters this field, the field changes, and the sensor's electronics detect that change.

The same five performance factors apply: target material, target size, target distance, sensor head size, and sensor mounting.

> **🟡 Capacitive proximity sensors can sense almost anything**, including non-metals like plastic, wood, paper, glass, and liquid. They detect metallic targets at greater distances than non-metallic targets. Two of the three wires go to the power supply, and the third (the output) sends a signal to a controller when something is sensed.

---

## Module 7: Electronic Sensor Applications

### Magnetic reed switch

The **reed switch** is purely mechanical despite being grouped with electronic sensors. It contains two thin ferromagnetic reeds inside a sealed glass tube. When a magnetic field comes near, the reeds are magnetized in opposite polarities and pull together, closing the circuit.

> **🟡 Key facts about the magnetic reed switch**
> A reed switch can **only sense a magnetic field**. The reed switch is **purely mechanical**. It has only two leads and acts as a **single-pole, single-throw switch (SPST)** that closes in a magnetic field. It needs **no external power** and is connected in series with the power supply and then the load or controller input terminal. **It handles AC or DC, but has extremely small current capacity.**

> **🟡 Critical wiring warning — the reed switch cannot be directly wired across the power supply.**
> The reed switch, when closed, provides a **short**. A short across a power supply produces a huge current that **welds the switch shut** and ruins it. The LED lamp or another load must always be in series with the reed switch. This is the single most important safety rule for working with reed switches in the lab.

The performance of a magnetic reed switch is affected by the target material, the type of current (AC or DC — although the switch can handle both), the orientation of the magnet, the strength of the magnetic field, the distance between the magnet and the switch, and the material between them. Magnets in different orientations can produce wildly different sensitivities.

> **🟡 Whenever a magnetic field passes through both reeds in the same direction, the reeds will be magnetized so that they repel each other**, which means the switch will not close. The magnet has to be oriented so that the two reeds end up with opposite polarities.

### Hall effect sensor

> **🟡 A Hall effect switch can only sense a magnetic field, but can use AC or DC.**

A Hall effect sensor contains a small piece of conductive material with current flowing through it. When a magnetic field is brought close, the field bends the path of the moving charge carriers, which causes a small but measurable voltage difference to appear across the material at right angles to the current flow. This voltage difference is called the **Hall voltage**, and it is what the sensor amplifies and uses to drive its output.

The performance of a Hall effect sensor depends on the strength and polarity of the magnetic field, the quality of the internal amplifier, and the target material. The Hall voltage produced directly by the effect is **small**, which is why amplification is so important. Hall effect sensors will only detect objects that have a **magnetic field** — they cannot directly detect plain steel the way an inductive sensor can.

### Photoelectric sensors

> **🟡 A photoelectric sensor energizes its output when it sees light.**
> A photoelectric sensor is a solid-state device that uses the principle of **photoconduction** — the ability of a material to conduct electrical current when struck by light. It has three components: the **light source (transmitter)**, the **photoelectric sensor (receiver)**, and the **electrical switch contacts**.

> **🟡 Photoelectric sensors come in two flavors**
> A **through-beam** sensor has the transmitter and receiver in separate housings facing each other. The object to be sensed breaks the beam to activate the sensor — when the light path is interrupted, the sensor switches. A **retro-reflective** sensor has the transmitter and receiver in the same housing, with a mirror or reflector across the gap; the light goes out, bounces off the reflector, and comes back to the receiver. The object to be sensed interrupts this reflected beam.

Photoelectric sensors have the **greatest sensing range** of almost all sensor types, but they may need to be shielded from direct sunlight or other strong light sources that could falsely trigger them.

🟡 Retro-reflective sensors must have a **sufficient amount of light reflected back from the mirror** in order to work. A subtlety here is that shiny, reflective objects can reflect the beam straight back to the sensor — exactly the wrong outcome, because that mimics the "no object present" condition. To prevent this, the sensor and its mirror are normally aimed not perpendicular to the conveyor or path; instead the angle is **far from perpendicular (near ~45 degrees)**, which ensures that only a properly aligned mirror at the proper distance returns the beam, while shiny passing objects scatter the light away.

Other factors that influence sensitivity are the size of the target, the distance to the target, and the shape of the target.

### Wiring tips for the four sensor families

> **🟡 Inductive and capacitive sensor wiring is identical.**
> Connect the power leads — +12 and ground. The only lead remaining is the signal lead, which is wired to the control input (in the lab, the indicator lamp substitutes for the control input). Both have two tiny LEDs built into the body: one lights when the sensor is properly powered, and the other lights when a target is sensed. If the tiny target-sensed LED on the sensor is on but the controller input does not light up, check the voltage at the controller input — the issue is between the sensor and the controller, not in the sensor itself.

The **reed switch** has just two wires. It works on AC or DC. Wire it in series with a load — never across the supply.

The **Hall effect** sensor has a power lead and a ground lead, and either a third signal output lead or a built-in switching arrangement, depending on the model. It also works on AC or DC.

The **photoelectric** sensor uses a similar three-wire scheme: a power lead, a ground lead, and a signal lead. There is sometimes a "spare" wire that, depending on the wiring, makes the sensor sense dark instead of light — this spare wire is not used for the standard lab exercises.

> **🟡 When any sensor doesn't work, always check supply voltages and output voltage** as the first troubleshooting step. Most problems turn out to be wiring or power issues, not bad sensors.


