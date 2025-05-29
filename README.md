**Name: SHREEDHAR KUMAR K.J**

**REGISTER NO: 212224230265
**

# EX NO: 6 - SYNCHRONOUS UP COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**PROCEDURE**

### 1. Open Quartus Software
Launch **Quartus Prime** on your system.

### 2. Create a New Project
- Navigate to **File > New Project Wizard**.
- Set your **project directory**, **project name**, and **top-level entity name**.
- Add your **Verilog (.v)** or **VHDL (.vhd)** source file.
- Select the correct **FPGA device** based on your target board.

### 3. Add Design Code
- Open your top-level module (e.g., `main.v`).
- Paste or write your Verilog/VHDL design.

### 4. Compile the Design
- Go to **Processing > Start Compilation**.
- Wait until the compilation process is complete.
- Resolve any errors or warnings if present.

### 5. Generate RTL Schematic
- Navigate to **Tools > Netlist Viewers > RTL Viewer**.
- View the generated RTL schematic.
- Save the schematic using **File > Export** (as image or PDF).

### 6. Assign I/O Pins
- Open **Assignments > Pin Planner**.
- Assign FPGA pins to your module’s inputs and outputs.
- Click **Save** once done.

### 7. Create Waveform for Simulation
- Go to **File > New > Other Files > Vector Waveform File (.vwf)**.
- Click **Edit > Insert > Insert Node or Bus**.
- Select all input and output signals to monitor.

### 8. Set Simulation Parameters
- Define end time using **Edit > End Time** (e.g., `1 us`).
- Apply different **input combinations** on the waveform.

### 9. Run Functional Simulation
- Go to **Processing > Start Simulation**.
- The **timing diagram** (simulation output) will be displayed.

### 10. Save the Timing Diagram
- Save the waveform for future reference.
- Export the timing diagram image via **File > Export Image**.
  

**PROGRAM**

![Screenshot 2025-05-05 125703](https://github.com/user-attachments/assets/79f8029d-6c4c-4132-afd3-0a162c89baa1)

**RTL LOGIC UP COUNTER**

![Screenshot 2025-05-05 125711](https://github.com/user-attachments/assets/afc35340-80c8-4f2b-ab0f-8b1a798280ac)

**TIMING DIAGRAM FOR IP COUNTER**

![Screenshot 2025-05-05 125650](https://github.com/user-attachments/assets/1709605c-3d10-4b61-ae47-eef736e2dcb2)


**TRUTH TABLE**

![Screenshot 2025-05-05 125938](https://github.com/user-attachments/assets/cc100817-c125-4d58-93bf-ce2a41c517f6)


**RESULTS**

Thus the 4 bit synchronous up counter is implemented and its functionality is validated.
