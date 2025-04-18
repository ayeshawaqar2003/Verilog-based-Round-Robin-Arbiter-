# Verilog-based-Round-Robin-Arbiter-
a Verilog-based Round-Robin Arbiter that enables fair and efficient allocation of resources among competing requests in a digital system. This arbiter system processes multiple simultaneous requests on a per-packet basis, providing equal access to each requester.
Design Approach
The arbiter employs a Finite-State Machine (FSM) structure to handle state transitions and prioritize requests in a systematic, round-robin manner. Each component is detailed as follows:
•	FSM Structure: The arbiter operates across states: Idle (S_IDLE) and active states (S_0, S_1, S_2, S_3), which correspond to each requester. Requests are prioritized cyclically in each state.
•	Round-Robin Counter: A counter cycles through requesters, granting access sequentially.
•	Dynamic Scanning: The system scans requests at each clock cycle or upon acknowledgment, ensuring responsiveness to active requests.
•	Bandwidth Reallocation: When a requester’s queue is empty, unused bandwidth is distributed among active requesters to optimize system resources.


Block Diagram / State Transition Diagram
A block diagram of the Round-Robin Arbiter is shown below, including its main modules:
1.	Input Interface - Manages incoming request signals.
2.	Round-Robin Counter - Cycles through requests.
3.	FSM Logic - Controls state transitions, ensuring fair allocation.
4.	Output Control - Generates grant signals for each active requester.

   ![image](https://github.com/user-attachments/assets/0dc5b2ec-1da9-4952-8a9e-923634767d4f)

 
                                                   Fig 2 State transition diagram

7. Design Choices and Implementation Logic
The design choices in this project include the following elements:
•	Time Slice Allocation: Each request is granted access for a defined time slice, improving predictability.
•	Request Handling: Requests are handled cyclically, ensuring fairness.
•	Output Generation: The GNT (grant) signal reflects access given to each requester in a round-robin sequence.
The Verilog Code encapsulates each design component, with a testbench to validate functionality across different scenarios. The following states outline the FSM-based approach:
1.	IDLE: No active requests; the arbiter waits.
2.	S_0 to S_3: Each state corresponds to one requester, which is granted access cyclically.




8. Truth Table
Here's a structured report for the project, based on the requirements and rubric outlined. This includes detailed sections covering the project’s objectives, problem statement, design, implementation, simulation, and conclusions.






![image](https://github.com/user-attachments/assets/65f7c196-beb3-4f44-ad48-9289028caa45)







![image](https://github.com/user-attachments/assets/83c8c149-dec1-4451-b7b1-5b227b191fbd)


RESOURCES:
1.	N. L. Venkataraman, S. Sumithra, R. Purushothaman, S. Kumar, K. Kokulavani, and V. Gowri, "Design of matrix, distributive round robin, ping pong and enhanced ping lock arbiter for shared resources systems," Indonesian Journal of Electrical Engineering and Computer Science, vol. 32, no. 3, pp. 1337-1345, Dec. 2023, doi: 10.11591/ijeecs.v32.i3.pp1337-1345.
2.	N. L. Venkataraman, S. Sumithra, R. Purushothaman, S. S. Kumar, K. Kokulavani, and V. Gowri, "Design and Implementation of Different Arbiter for Shared Resource Systems," in Trends in Advanced Engineering Research, vol. 4, Ch. 4, ISBN: 978-81-969723-3-2, eBook ISBN: 978-81-969723-0-1, doi: 10.9734/bpi/taer/v4/2779G.
3.	A. Toe, "Design and verification of a Round-Robin Arbiter," M.S. thesis, Dept. Elect. and Microelectron. Eng., Kate Gleason Coll. of Eng., Rochester Inst. of Technol., Rochester, NY, USA, 2018.



