# Operating-Systems
In this repo, I'll try to talk about OS

![image](https://github.com/user-attachments/assets/0abb0ce4-5ba6-4dd0-b9b5-465e96979e8f)

- Operating systems are an essential part of any computer system. Similarly, a course on operating systems is an essential part of any Computer Science as well as Electronics course. This field is undergoing rapid change, as computers are now prevalent in virtually every application. Yet the fundamental concepts remain fairly clear and that is what will be taught in this course.
- In brief, an operating system acts as an intermediary between the user of a computer and the computer hardware. The purpose of an operating system is to provide an environment in which a user can execute programs in a convenient and efficient manner. 
Every important aspects of an Operating System will be taught in this course so as to get a proper understanding about Operating Systems and their design and working.

- You will find them on the following topics:
1. Introduction to OS.

2. Operating System Structures.

3. Process Management  
   3.1 Processes  
   3.2 Threads  
   3.3 CPU Scheduling  
   3.4 Process Synchronization  
   3.5 Deadlocks  

4. Memory Management  
   4.1 Main Memory  
   4.2 Virtual Memory  

5. Storage Management  
   5.1 File System Interface  
   5.2 File-System Implementation  
   5.3 Mass-Storage Structure  
   5.4 I/O Systems  

6. Protection and Security  

7. Distributed Systems
   7.1 Distributed System Structures  
   7.2 Distributed File Systems  
   7.3 Distributed Coordination  

8. Special Purpose Systems  

---

###  Introduction to OS
- An Operating System (OS) is a program that manages the computer hardware.
- It also provides a basis for Application Programs and acts as an intermediary between computer User and compter Hardware.
- Examples of widely used OS include Windows, Linux, Ubuntu, macOS, iOS, and Android. Let's take an overview of what an OS is, its functions, and its various types.
![image](https://github.com/user-attachments/assets/97fb27a2-382b-4819-9653-17b3593c84a7)
---

- The computer system comprises several components: at the base level is hardware including the CPU, memory (RAM and ROM), and I/O devices such as keyboards and monitors. The Operating System (OS) sits above the hardware, managing resources and providing a platform for system and application software.
- System software operates directly on the hardware, while application software runs on top of the OS.
- This structure illustrates how the OS interacts with both hardware and software to facilitate computing tasks.
![image](https://github.com/user-attachments/assets/14ec5d30-bd5d-48d8-8ec6-8b2ca4e61766)
- System software, including the Operating System (OS), manages computer hardware and enables system operations, while application programs are designed for end-user tasks.
- Examples of application programs include word processors like Microsoft Office Word, spreadsheets like Microsoft Excel, compilers for code writing, text editors like Notepad, and web browsers like Google Chrome. These programs perform specific functions and are used directly by users to accomplish various tasks.
- Without an Operating System (OS), users would have to communicate directly with computer hardware for every task, which involves complex coding for actions like opening applications, typing, displaying text, and saving files. This would make even simple tasks cumbersome and impractical.
- The OS acts as an intermediary, simplifying interactions between users and hardware by managing these tasks and allowing users to perform actions more intuitively, such as double-clicking an application icon to start a program.
- The Operating System (OS) simplifies user interaction with computer hardware by handling all underlying tasks. When a user performs actions like typing or saving a document, the OS manages these operations behind the scenes, including opening applications, displaying text, and allocating memory. This allows users to focus on their tasks without needing to manually code every interaction with the hardware. Essentially, the OS acts as an intermediary, making computing easier and more accessible by managing complex hardware interactions.

---

- Operating systems (OS) serve as intermediaries between users and hardware, facilitating seamless computing experiences.
- Key types of OS include batch, time-sharing, distributed, network, real-time, and multi-tasking systems, each designed for specific needs.
- The main functions of an OS include acting as an interface between users and hardware, and allocating resources like the CPU and memory. Understanding these types and functions provides a foundation for exploring how different OS designs cater to various computing requirements.
- Operating systems (OS) are crucial for managing computer resources, including memory and input-output devices. They allocate resources efficiently to users and processes, ensuring that limited hardware is utilized effectively. Key functions include managing memory, ensuring security, and facilitating resource allocation. The primary goal of an OS is to provide convenience by simplifying user interactions with hardware, making computing tasks more manageable and less tedious.
- Efficiency in operating systems involves the effective management of computer resources, ensuring that all users receive appropriate amounts of resources without manual intervention. An OS handles the allocation of resources and management of memory, which is crucial for maintaining optimal performance and avoiding wastage. By automating these tasks, the OS enhances system efficiency, balancing the needs of multiple users and processes effectively. This goal complements the OS's role in providing convenience and is central to its overall design and functionality.
![image](https://github.com/user-attachments/assets/75db71ad-a7a2-479c-95e5-a8a89bb40001)
---

#### Basics of OS (Computer System Operation)
##### Some basic knowledge of the structure of Computer System is required to understand how Operating Systems work.
- A modern general-purpose computer system consists of one or more CPUs and a number of device controllers connected through a common bus that provides access to shared memory.
![image](https://github.com/user-attachments/assets/6ae4eb11-5743-4dec-b600-f3d45b7f6cec)
---

##### Undertanding the role of CPUs in modern computer systems
- A modern computer system typically includes one or more central processing units (CPUs), which are crucial for performing all computational tasks.
- The CPU, often confused with the entire computer case, is actually a small chip embedded in the motherboard responsible for calculations and processing.
- The system may also contain various device controllers connected through a common bus to manage hardware components like disks, keyboards, and printers, all of which interact with the CPU to perform their functions.

##### How Device Controllers Manage Hardware and Memory Access
- Device controllers, such as USB controllers for peripherals and video adapters for displays, manage specific hardware components by regulating their operation.
- These controllers, along with the CPU, are connected through a common bus to shared memory.
- This shared memory, often RAM, is finite and must be managed carefully as both the CPU and device controllers can compete for access to it.
- Each controller is responsible for ensuring the proper functioning of its respective device while interfacing with the shared memory through the common bus.

##### The Role of Memory Controllers in Concurrent Device Operations
- To handle multiple device operations simultaneously without lag, a memory controller is used to synchronize access to the main memory.
- When devices such as disk controllers and input peripherals operate concurrently, they all need to access the shared memory for execution.
- The memory controller ensures that each device and the CPU get their required share of memory, managing access efficiently to prevent conflicts and maintain smooth operation across all devices.
![image](https://github.com/user-attachments/assets/406b8ad4-31d6-40c4-9b1c-cde2b235444d)
---

##### The Role and Function of the Bootstrap Program in System Startup
- The bootstrap program, also known as the bootloader, is the first program executed when a computer is powered on or rebooted. Stored in ROM (Read Only Memory).
- It initializes the system by loading the operating system from secondary memory into the main memory.
- This program is essential for starting the operating system and facilitating the interaction between the user and the computer's hardware, ensuring that the system boots up properly and is ready for use.

##### The Bootstrap Program's Role in Loading the OS Kernel
- The bootstrap program is responsible for initiating the computer system by locating and loading the operating system's kernel into the main memory.
- The kernel, which is the core component of the operating system, must be loaded for the OS to become operational.
- This process occurs immediately when the computer is powered on, ensuring that the system is prepared for further operations and management by the operating system.

##### Understanding the Role of Interrupts in CPU Operations
- Interrupts are signals sent by hardware or software to the CPU, requesting it to halt its current task and address a more urgent one.
- This mechanism allows the CPU to manage multiple tasks efficiently by pausing ongoing processes to handle higher-priority operations.
- Interrupts ensure that critical tasks are addressed promptly, maintaining the system's responsiveness and functionality.
![image](https://github.com/user-attachments/assets/edca9f00-bf38-4a00-9f34-75ad4b119e79)
---

##### Understanding System Calls and Their Function
- System calls, also known as monitor calls, are special operations triggered by software that cause an interrupt in the CPU. Unlike hardware interrupts, which come from external devices, system calls originate from within the software. When a system call is made, it interrupts the CPU's current task and transfers execution to a predefined location where the service routine for the call is executed, allowing the system to handle specific requests or operations.
![image](https://github.com/user-attachments/assets/9124766b-8870-4f87-a303-766302c3e1f8)
---

#### Basics of OS (Storage Structure)
##### Understanding the Hierarchical Structure of Computer Storage Devices
- The hierarchy of computer storage devices is critical for understanding their roles and functions.
- At the top of this hierarchy are Registers, which are the smallest and fastest storage units, storing data in bits.
- They are followed by Cache, which is larger but slightly slower than Registers.
- Main memory is essential for active processes, while Electronic disks, Magnetic disks, Optical disks, and Magnetic tapes represent progressively larger and slower storage options.
- This structure illustrates how different types of storage contribute to the overall efficiency and performance of a computer system.

##### Exploring the Differences Between Main and Secondary Storage Devices
- Main memory, such as Random Access Memory (RAM), plays a crucial role in a computer's performance by providing fast access to data currently in use. In contrast, secondary storage devices like Electronic disks, Magnetic disks, Optical disks, and Magnetic tapes serve as larger, more cost-effective options for long-term data storage.
- The hierarchy of these storage types indicates that as you move up, the devices become smaller and more expensive, while access time improves.

##### Understanding the Role of Main Memory in Computing Systems
- Main memory, specifically Random Access Memory (RAM), serves as the critical workspace where data and programs are loaded for execution. While it allows for fast access and processing, it is limited in size and volatile, meaning data is lost when power is turned off.
- Secondary memory, including Electronic disks, Magnetic disks, Optical disks, and Magnetic tapes, is used to store larger amounts of data and programs that are not currently in use.
- This hierarchical relationship between main and secondary memory highlights the balance between speed, capacity, and volatility in computer systems.

##### The Importance of Main Memory for Software Execution
- Main memory, or RAM, is essential for executing software applications. When a program, such as Microsoft Word, is installed, it resides in secondary memory until activated. Upon opening, the program is loaded into main memory, allowing for fast processing and execution of tasks.
- The speed of a computer is significantly influenced by the amount of RAM; more RAM facilitates smoother and quicker operations.
- This relationship emphasizes the role of main memory in enhancing overall computing performance, as it temporarily holds active programs and data needed for immediate access.

##### Analogies to Understand Main Memory and Secondary Storage
- The analogy of a bookshelf and a table effectively illustrates the relationship between secondary memory and main memory.
- The bookshelf represents secondary storage where all data is kept, similar to how books are stored. When a user wants to access data, they take it from the bookshelf and place it on the table, which symbolizes the main memory (RAM) where active data is processed. If the table is small, only one book can be placed at a time, highlighting the limitations of insufficient RAM; this restricts the ability to multitask or reference multiple data sources simultaneously.

##### The Impact of Main Memory Size on Computer Performance
- The size of main memory (RAM) directly influences a computer's ability to perform tasks efficiently. Just as a small table limits the number of books that can be studied at once, a smaller main memory restricts how much data can be loaded and processed simultaneously, resulting in slower performance. In contrast, a larger main memory allows for more data to be accessed quickly, improving overall speed and functionality. Additionally, main memory is volatile, meaning it loses its data when power is removed, unlike secondary memory, which retains information.

##### Now let's try to understand the meaning of volatile and non-volatile
- Volatile memory, such as RAM, loses its contents when power is cut off, meaning any stored data is permanently erased. In contrast, nonvolatile memory, like hard drives and flash storage, retains information even when power is removed. This key difference is crucial for understanding how data is managed and preserved in computing systems, impacting both performance and data integrity.
- Nonvolatile memory is designed to retain its stored data even when the power supply is turned off. This characteristic allows devices such as hard drives, flash drives, and ROM to preserve information, ensuring that it remains accessible for future use regardless of power status. This capability is essential for long-term data storage and retrieval in various computing applications.
- Registers, cache, and main memory are classified as volatile storage, meaning they lose data when power is off. In contrast, secondary storage devices like electronic disks, magnetic disks, optical disks, and magnetic tapes are nonvolatile, retaining data even without power. Understanding these differences is crucial for effective data management and system performance.

##### The Role of Battery Backup in Nonvolatile Memory Types
- Nonvolatile RAM, such as NVRAM, utilizes a battery backup to maintain data even when the main power is turned off. This feature distinguishes it from standard volatile memory types like registers, cache, and main memory, which lose their contents without power. Understanding these special cases enhances the knowledge of memory management in computing.

- In this pic, The cost per bit and access time decrease down the hierarchy not increase as it mentioned.
![image](https://github.com/user-attachments/assets/f1ed2f54-ab2a-4ebe-94ad-d4e4943293ac)

---

#### Basics of OS (I/O Structure)
- Let's make the obscure concepts clear.
- An I/O device is connected to the machine by I/O port. And the devices have their dedicated device controller.
- Device controller is nothing but intermediate hardware between the machine, I/O device and OS. The OS sends instructions to the CPU to manipulate I/O devices.Then CPU sends signals to these devices via device controller (of course, not only CPU,  device controllers have registers inside too). 
- But how does OS know what device is connected and what instructions should it send to get device working? 
- When a manufacturer makes a device, they will distribute its driver program along with it. This is because the OS will never have idea about the device. The only way to interact with the device is by talking to its driver program.
- Lots of beginners think the OS will have full understanding of a device once the driver is installed, which is NOT true. Driver will never become a part of OS.
- It is the driver program sends instructions and receives data from the device and pass it to OS for use. The OS and Driver can talk to each other simply because they are both loaded on the memory.
- You can think a driver as a daemon program, which long time resides on the memory space until system shuts down.
- Above all, is why I/O device (those shinny RGB keyboards) stops working as soon as driver program crashes.

![image](https://github.com/user-attachments/assets/f71e9a7e-7711-4416-88d2-3dc134dc4294)

##### Working of an I/O operation:
1. Loading Registers: The device driver tells the device controller what to do by loading values into its registers.
2. Controller Action: The device controller reads these values from its registers and knows what operation to perform.
3. Data Transfer: The device controller moves data between its local buffer and the CPU's memory as instructed.
4. Interrupt: When done, the device controller sends an interrupt to the CPU to let it know that the operation is complete.
5. CPU Response: The CPU stops its current task, handles the interrupt, and processes the data transferred by the device controller.
![image](https://github.com/user-attachments/assets/bb15e09f-29fe-4077-bf9a-6e017e4624c2)
![image](https://github.com/user-attachments/assets/486657f2-5fe6-40bc-b366-22a580a74706)

---

#### Computer System Architecture
##### Understanding the Categories of Computer System Architectures
- Computer systems can be categorized based on the number of general-purpose processors they utilize.
- The main types include single processor systems, which rely on one CPU to execute tasks, and multiprocessor systems, which incorporate two or more CPUs to enhance performance. Additionally, clustered systems link multiple systems to work collaboratively on tasks, thus improving efficiency and processing power.
- Each architecture has its own advantages and specific use cases, highlighting the diverse capabilities of computer systems.
![image](https://github.com/user-attachments/assets/1a543b17-fc15-48a9-8fc7-873246921956)

---

##### Single Processor Systems
- A system is categorized as a single processor system based on the number of general-purpose processors it contains.
- In addition to general-purpose processors, computer systems also contain special purpose processors designed for specific tasks related to individual devices.
- For instance, a keyboard includes a microprocessor dedicated to converting keystrokes into a binary code that the computer can understand. These special purpose processors do not perform general computing tasks but focus solely on their designated functions, enhancing the overall efficiency of device operation. Despite their presence,
![image](https://github.com/user-attachments/assets/f99ddb4e-4979-453c-bc78-6b3830c0dfaf)

---

##### Multi Processor Systems
- Multiprocessor systems consist of two or more processors that operate in close communication, sharing resources like the computer bus, clock, memory, and peripheral devices.
- This architecture, often referred to as a parallel system or tightly coupled system, enables the processors to work collaboratively on single or multiple tasks, enhancing efficiency and performance.
- One of the key advantages of multiprocessor systems is increased throughput, which measures the system's performance by quantifying the amount of data that can be processed or transferred at a given time, ultimately leading to improved computational capabilities.
- Throughput is something that we can use to measure the performance of our system that's because we have more than one processor which parallelly do our work and it will make it faster and more efficient. so sometimes it is also known as the amount of data that can be transferred from one location to another.

###### Key Advantages of Using Multiprocessor Systems
- Multiprocessor systems provide several key advantages over single processor systems, primarily through increased throughput, economy of scale, and enhanced reliability.
- With multiple processors working in parallel, tasks can be completed more quickly and efficiently, leading to higher performance. Economically, these systems share resources among processors, reducing the need for multiple single processor setups that would require separate resources. Additionally, if one processor fails, the remaining processors can continue functioning, ensuring greater reliability and minimizing downtime, making multiprocessor systems a more robust choice for computing needs.
- Even if a single processor fails, we still have processors which will back us up and keep us running, so your system will still work even though the performance may reduces a bit. not like in single processor systems, if single processor fails, that means it is a total failure and your whole system breaks down.
![image](https://github.com/user-attachments/assets/67b24a94-8eb7-4416-a606-58730eeb6a0e)

###### Types of Multi Processor Systems
1. Symmetric Multiprocessing (SMP):
- Multiple CPUs (CPU 1, CPU 2, CPU 3) are connected to a shared memory or resource pool.
- Each CPU has equal access to all tasks (P1, P2, P3) and works independently to process them.
- There is no hierarchy among the processors; all CPUs can run tasks independently and work on any process.

2. Asymmetric Multiprocessing (AMP):
- A master-slave configuration is used, where the master processor coordinates the work of the slave processors.
- The master processor assigns specific tasks (P1, P2, P3) to the slave processors (Slave 1, Slave 2, Slave 3).
- The master controls the system, and the slaves depend on it for task allocation.
![image](https://github.com/user-attachments/assets/f52b3527-1c57-486a-84ab-daaeb0e35f51)
---

##### Clustered Systems
- Clustered systems are designed by coupling two or more individual computer systems to work together on computational tasks, providing distinct advantages over traditional multiprocessor systems. Unlike multiprocessor systems, which consist solely of multiple processors within a single machine, clustered systems integrate entire systems, allowing for greater fault tolerance.
- This design enhances high availability, as the failure of one system does not result in complete operational failure; the remaining systems can continue to handle the workload.
- Additionally, clustered systems can be organized in either symmetric or asymmetric configurations, offering flexibility in architecture and resource management.

###### Comparison of Symmetric and Asymmetric Clustered Systems
- Clustered systems can be structured in two main ways: symmetric and asymmetric.
1. Asymmetric clustered systems, one machine operates in a hot-standby mode, monitoring the others that are actively running applications. If any of these active systems fail, the standby machine takes over, ensuring continuity.
2. Symmetric clustered systems involve multiple hosts that not only run applications but also monitor each other, allowing for better resource sharing and efficiency. Symmetric configurations are generally preferred due to their collaborative nature, which optimizes resource usage and enhances system reliability.
![image](https://github.com/user-attachments/assets/23d9d312-e157-43f2-b652-e618dda31a3e)
---

### Operating System Structure
#### Multiprogramming & Multitasking
##### Understanding the Structure of Operating Systems in Detail
- This lecture focuses on the internal structure of operating systems, emphasizing the differences and commonalities among various types such as Windows and Ubuntu.
- It introduces key concepts of multiprogramming and multitasking, explaining that all operating systems must support these functionalities.
- Multiprogramming allows multiple programs to be executed simultaneously by the CPU, which is essential for efficient resource utilization.
![image](https://github.com/user-attachments/assets/3ce2dd9e-9f8d-4347-b53d-515a9a9d3f21)
---

#### Multiprogramming
##### The Importance of Multiprogramming for CPU Utilization
- Multiprogramming enhances CPU utilization by allowing multiple programs to be loaded and executed concurrently, preventing idle time for the CPU and I/O devices.
- When a single user operates without multiprogramming, they can monopolize these resources, leading to inefficiencies. By organizing jobs—comprising code and data—into a job pool, multiprogramming ensures that the CPU always has tasks to execute.
- This system improves overall resource management and responsiveness, enabling better performance and productivity in computing environments.
##### Managing Limited Memory with Multiprogramming Techniques
- Multiprogramming is crucial in systems with limited main memory, such as a 512 MB RAM environment, where not all jobs can be loaded simultaneously.
- In this setup, only a subset of jobs can reside in memory at any time. Without multiprogramming, when a job like 'Job 1' requires I/O resources, the CPU becomes idle until the job completes, leading to inefficiencies. However, with multiprogramming, when 'Job 1' waits for I/O, the CPU can be reassigned to another job, ensuring that CPU resources are utilized effectively, thereby optimizing overall system performance.
##### Efficiency of Multiprogramming in Resource Utilization
- Multiprogramming significantly enhances CPU efficiency by allowing multiple jobs to utilize CPU resources without idleness.
- When a job, like 'Job 1', requires I/O operations, the CPU can be assigned to another job, such as 'Job 2', ensuring continuous resource use. This dynamic reassignment prevents the CPU from remaining idle, optimizing overall system performance.
- The analogy of a lawyer managing multiple clients illustrates this concept, demonstrating how resources can be effectively utilized in various scenarios. For an operating system to function efficiently, it must support multiprogramming to manage CPU, memory, and other resources effectively.
![image](https://github.com/user-attachments/assets/8d72a93f-6c49-46a1-9342-ef6ad25f037f)
---

#### Multitasking (Time-shared OS)
##### Key Differences Between Multiprogramming and Time Sharing Systems
- Time sharing, or multitasking, differs from multiprogramming by enabling user interaction with multiple jobs concurrently. While both systems execute multiple jobs, time sharing allows the CPU to switch rapidly among them, providing a seamless experience where users can engage with programs while they are running. This quick context switching facilitates direct communication between the user and the computer system, enhancing interactivity. In contrast, multiprogramming primarily focuses on resource utilization without offering real-time user engagement, making time sharing essential for interactive computing environments.
##### Understanding Time Sharing Systems and User Interaction
- Time sharing systems enable multiple users to share computer resources simultaneously, creating an environment where each user perceives the system as dedicated to them.
- This is achieved through rapid job switching, which occurs so quickly that users are often unaware they are sharing the system. For example, in a scenario with four users, each feels as if they have exclusive access to the system while they are actually sharing it.
- The efficiency of the CPU allows for swift execution of jobs, enhancing the user experience and interaction with the system. This approach fosters direct communication between users and the system, making time sharing essential for modern computing.
##### The Interaction Dynamics in Time Sharing Systems Explained
- In time sharing systems, the execution of jobs occurs at CPU speed, while user interaction happens at a much slower human pace. After a job is executed, users receive output and provide new input, creating a significant time gap due to the disparity between the fast CPU and slower human input. During this gap, the CPU can process tasks for other users, allowing for efficient resource utilization. This rapid switching and scheduling make users feel as though they have exclusive access to the system, even though they are sharing it with others. The combination of CPU scheduling and multiprogramming is essential for maintaining this seamless user experience.
##### Understanding Processes and Their Role in Time Sharing Systems
- In time sharing systems, each user perceives the entire computer system as dedicated to them, despite sharing it with others.
- The distribution of system time among users is managed by CPU scheduling algorithms, which determine how resources are allocated.
- Each user has at least one program waiting in memory, which is referred to as a process when it is loaded and executing.
![image](https://github.com/user-attachments/assets/078573ca-0aec-4b8e-90e3-6a55620df5a9)
![image](https://github.com/user-attachments/assets/4b6b69b7-b990-4cd8-aad0-97234e8457b9)
---

#### Operating System Services
- An OS provides an environment for the execution of programs.
- It provides certain services to programs and to users of those programs.
![image](https://github.com/user-attachments/assets/964daf86-e177-4b7d-af20-3332fac731fa)
---

- User Interface: Facilitates interaction between the user and the operating system, typically through graphical user interfaces (GUIs) or command-line interfaces (CLIs).
![image](https://github.com/user-attachments/assets/0e6f46ad-7d60-4d27-931e-5cd00d0fe3d4)
---

- Program Execution: Manages the execution of programs by loading them into memory, running, and terminating them.
![image](https://github.com/user-attachments/assets/bcc440f7-7b37-4b76-a2a0-7442a39cce8f)
---

- I/O Operations: Handles input and output operations, enabling interaction between the system and external devices like keyboards, printers, and storage drives.
![image](https://github.com/user-attachments/assets/cde5615a-ff59-4959-bf88-2ff0e62fb887)
---

- File System Manipulation: Manages file operations such as creating, deleting, reading, and writing files on storage devices.
![image](https://github.com/user-attachments/assets/3cccccbe-7d6d-42d6-b667-43970df02e6e)
---

- Communications: Facilitates data exchange between processes running on the same or different systems, using shared memory or message-passing mechanisms.
![image](https://github.com/user-attachments/assets/f9383b32-256b-49b3-8800-4eba62124920)
---

- Error Detection: Continuously monitors the system for potential errors, including hardware failures and software issues, and responds appropriately.
![image](https://github.com/user-attachments/assets/4f05172c-74fe-4c8f-b4ac-42d706e98192)
---

- Resource Allocation: Allocates and manages resources like CPU time, memory, and I/O devices among multiple processes.
![image](https://github.com/user-attachments/assets/7a26b42e-1fa2-4a10-b1e8-64aa3541d6b7)
---

- Accounting: Tracks system usage by users and applications, helping in auditing and optimizing resource usage.
![image](https://github.com/user-attachments/assets/6e0ff195-490e-473e-86b5-7b332a3b85c3)
---

- Protection and Security: Ensures controlled access to system resources, protecting data and system integrity from unauthorized access or breaches.
![image](https://github.com/user-attachments/assets/fe037494-719d-4cf2-aae1-e749a2439d00)
---

#### User Operating System Interface
##### Understanding the User Operating System Interface Approaches
- This key point explores the two fundamental approaches for user interaction with operating systems: the Command Line Interface (CLI) and the Graphical User Interface (GUI).
- The CLI allows users to input commands directly, requiring them to remember specific syntax for tasks, while the GUI provides a more visual and intuitive way to interact with the system through graphical elements. Each approach has its own advantages and use cases, influencing user experience and efficiency.
##### Exploring Command Line and Graphical User Interfaces in Operating Systems
- The GUI is characterized by its user-friendly design, allowing interaction through visual elements like desktops and menus, which enhances usability for everyday tasks. In contrast, the CLI requires users to input text-based commands, necessitating knowledge of specific command syntax. Additionally, the command interpreter's implementation varies, as some operating systems integrate it into the kernel, while others treat it as a standalone program, affecting performance and functionality.
##### Understanding Command Interpreters and Shells in Operating Systems
- This key point highlights the role of command interpreters, also known as shells, in various operating systems like Windows and Linux.
- In Windows, the Command Prompt (CMD) serves as the CLI, while Linux utilizes the Terminal. Users may encounter different types of shells, such as Bourne Shell, C Shell, and BASH (Bourne-Again Shell), each offering unique functionalities. The command interpreter can execute tasks by containing the necessary code for operations, allowing users to perform actions like creating, deleting, or renaming files efficiently.
![image](https://github.com/user-attachments/assets/ed3bbf46-fc45-48d9-9cf2-5435b422d4b6)
![image](https://github.com/user-attachments/assets/234b634b-3093-4005-86b1-1f7bb3cef973)
---

#### System Calls
##### Understanding the Role of System Calls in Operating Systems
- System calls are essential interfaces that connect user applications to the services provided by the operating system.
- They enable programs to request services such as file operations, process management, and communication.
- Programs operate in two distinct modes: user mode and kernel mode.
- User mode restricts access to critical system resources, ensuring stability and security. In contrast, kernel mode allows programs direct access to hardware and memory, granting them elevated privileges. However, executing in kernel mode poses risks, as a crash can lead to system-wide failures, highlighting the importance of carefully managing system calls.
- Switching from kernel to user and vice versa is known as mode shifting not context switch. Context switch is the one which happens between 2 processes.
##### There are 2 modes of execution for a program:
1. User mode: 
- Do not have access to resources like memory or hardwares.
- When a program crashes, the entire system will not break down.

2. Kernel mode:
- Privilidged mode.
- Have access to resources.
- When a program crashes, the entire system breaks down.

- Because user mode is safer, most programs run in user mode. But some programs might need access to resources, so they will make a call to the OS to request for these. This call is system call. 
- When the OS receives the system call, it will change the mode of the program to kernel mode. This is called mode shifting.
![image](https://github.com/user-attachments/assets/a3d00d93-add8-4e83-a1b5-60fb7ab64a8b)
![image](https://github.com/user-attachments/assets/da1ca864-9950-42b4-bc0b-1b3f601037ce)
---

- Example of a System Call sequence for writing a simple program to read data from one file and copy them to another file.
![image](https://github.com/user-attachments/assets/f1a654a8-0d63-4351-ab66-d5391cce483c)
---

#### Types of System Calls
![image](https://github.com/user-attachments/assets/1a7b60fa-6f88-4597-ac6e-cf9f03e240c4)

---

- Process Control: These system calls are used to create, modify, and manage processes and threads, including functions such as fork(), exec(), wait(), and exit().
![image](https://github.com/user-attachments/assets/d9561106-1cdd-4bff-9ece-866294b4bd0b)
---

- File Management: These system calls are used to create, modify, and manage files and directories, including functions such as open(), read(), write(), and close().
![image](https://github.com/user-attachments/assets/82a1a901-13b8-4899-93b9-edd9ad2a89e9)
---

- Device Management: These system calls are used to access and manage hardware devices such as printers, disks, and network interfaces, including functions such as ioctl() and read().
![image](https://github.com/user-attachments/assets/a2a3019a-ba31-4bfd-b104-44f031a5fa44)
---

- Information Maintenance: These system calls are used to retrieve and update information about the system and its resources, including functions such as getpid(), getuid(), and getgid().
![image](https://github.com/user-attachments/assets/85142dc8-0fbf-462c-962d-a17f00f0baf9)
---

- Communication: These system calls are used to facilitate interprocess communication and synchronization, including functions such as pipe(), socket(), and sendmsg().
![image](https://github.com/user-attachments/assets/0d65d6a8-8860-4fbb-8adf-49570c396be6)

- Memory Management: These system calls are used to allocate and manage memory resources, including functions such as mmap(), malloc(), and brk().
---

#### System Programs
##### Understanding the Role and Importance of System Programs in Computing
- System programs serve as a critical layer in the computing hierarchy, positioned directly above the operating system and below application programs.
- They facilitate interaction between the user and the hardware, providing essential functionalities like file management, process control, and hardware access. Examples include command interpreters and system utilities, which enhance system efficiency and usability. By comprehending the structure and purpose of system programs, one can better appreciate their significance in modern computing environments.

![image](https://github.com/user-attachments/assets/28946a7c-8a55-42cf-89a7-44e2eedfaefc)

---

##### System programs can be divided into the following categories

![image](https://github.com/user-attachments/assets/da59b435-5f35-4656-ad1a-419eb3569384)

---
![image](https://github.com/user-attachments/assets/578740b2-ee5b-42d5-bc31-e0c717508765)

---
![image](https://github.com/user-attachments/assets/9b81e95b-bbd4-493a-b369-c2e914ce463f)

---
![image](https://github.com/user-attachments/assets/f12db648-7ffd-4ddc-a93a-8f83bf18c282)

---
![image](https://github.com/user-attachments/assets/5d99cb4a-da4e-4744-b3ec-ec8772c0a249)

---
![image](https://github.com/user-attachments/assets/df28d586-a86d-4023-9c24-01c69f703603)

---
- In addition to systems programs, most operating systems are supplied with programs that are useful in solving common problems or performing common operations.
- Keep in mind that these are not system programs but these are application programs which are provided along with the OS for the users to perform certian tasks.
![image](https://github.com/user-attachments/assets/db8e0f6a-f358-49d4-87b5-a54bebaaaf17)
---

#### Operating System Design & Implementation
##### Challenges in Defining Goals for Operating System Design
- Designing an operating system involves overcoming the challenge of defining clear goals and specifications.
- This complexity arises from the varied user needs and system requirements, which may not align with a single set of goals. Consequently, it becomes difficult to satisfy all requirements simultaneously.
- Two primary factors influencing these goals include the choice of hardware and the types of systems to be implemented, such as multiprocessing or real-time systems, which further complicates the design process.
![image](https://github.com/user-attachments/assets/91ed0925-c7dd-4e40-8ec3-67876a6f1783)
---

##### Balancing User and System Goals in Design Challenges
- In operating system design, a key challenge lies in balancing user goals and system goals.
- User goals focus on convenience, ease of use, reliability, safety, and speed, reflecting the expectations of the end-users. Conversely, system goals emphasize the needs of designers and developers, prioritizing ease of design, implementation, maintenance, flexibility, reliability, and efficiency.
- These differing priorities can create complexities, as the vague nature of these requirements often lacks a clear formula for fulfillment, making it difficult to achieve a comprehensive solution.
![image](https://github.com/user-attachments/assets/8b1e9131-bd22-4d73-b882-36d3ecef8ffe)
---

##### The Role of Mechanisms and Policies in System Design
- In operating system design, there are no definitive rules for creating a system that is easy to learn and use. However, principles from software engineering provide frameworks that can address some of the design requirements.
##### Two critical concepts in this context are mechanisms and policies:
- Mechanisms refer to the methods or processes used to achieve a goal, while policies determine the goals themselves.
- Understanding these concepts helps in establishing effective strategies for system design, even in the absence of a one-size-fits-all solution.
![image](https://github.com/user-attachments/assets/16224f52-24a4-440b-b1f4-326b7534f9c3)
---

##### Implementation:
- Once an operating system is designed, it must be implemented.
- Traditionally, operating systems have been written in assembly language. 
- Now, however, they are most commonly written in higher-level languages such as C or C++

##### Advantages of writing in high level languages:
1. The code can be written faster
2. It is more compact
3. It is easier to understand and debug
4. It is easier to port

- E.g. MS-DOS was written in Intel 8088 assembly language. Consequently, it is available on only the Intel family of CPUs.
- The Linux operating system, in contrast, is written mostly in C and is available on a number of different CPUs, including Intel 80X86, Motorola 680X0, SPARC, and MIPS RXO00.
---

#### Structures of Operating System
- There are 5 types of structures for operating system:

##### 1. Simple structure
- The simple structure refers to the foundational design used in early operating systems, exemplified by MS-DOS.
- Every layers can access to the hardware.
##### Exploring the Vulnerabilities of Direct Hardware Access in MS-DOS
- In MS-DOS, application programs have direct access to base hardware, which resembles a layered structure but lacks true separation.
- Weak security.
![image](https://github.com/user-attachments/assets/cdac2af5-1fa3-4cec-add1-9c27aaff8886)
---

##### 2. Monolithic structure
- The monolithic structure of early Unix systems places all functionalities within a single kernel level.
- Hard to maintain, debug.
![image](https://github.com/user-attachments/assets/9b4d2309-1b4d-4240-a811-51dd294eeace)
---

##### 3. Layered structure
- The layered operating system design organizes functionalities into distinct layers, enhancing clarity and separation of concerns.
- Each functionality is one layer.
- One layer can only communicate directly with the layers above and below it.

##### Advantages of Layered Structure:
- The hardware is protected from the layers above, unlike the simple structure the user interface cannot directly access the system hardware.

##### Disadvantages of Layered Structure:
- U have to be very careful and specific in designing and deciding which will be the layers on top of a particular layer or which will be the layers below the particular layer, because a layer can only use those layers which are below that layer, only the services below it can be used by a particular layer.
###### In order to make this clear let's take an example:
- let's say that we're having a layer which deals with the backing storage, so we have to make sure that it has to be below the layer that deals with memory management, because the memory management routines needs to use the services provided by the backing storage.

- Let's take another problem, when one layer wants to use the services provided by the layers below it, the request has to go down below each layer one by one and by the time the service actually provided it may be late and not very fast.
###### In order to make this clear let's take an example:
- Let's say that a user program from this Layer N wants to execute an I/O operations, so in order to execute I/O operations it has to get the service from the Layer 0(Hardware) because I/O devices are falling under this Hardware, so what it will do? it will issue a system call in order to use the hardware and the system call has to go through this layers one by one until it reaches the Layer 0, so as the system call passes through these layers the parameters of the system call may be modified and it will take time in reaching there and then once the system call is granted then it will be able to use the I/O devices.
![image](https://github.com/user-attachments/assets/55f75570-2b8d-4137-bada-948fd50d4a40)
---

##### 4. Microkernels
- Instead of having so many functionalities like in monolithic kernel, what happens is that in this micro kernel approach we remove all the nonessential components from the kernel and we implement them as system and user level programs.
- The main function of this microkernel is to provide communication between the client program and these services, In contrast in the monolithic when the client program requesting for some kind of services it will have to ask a service from the kernel because everything is there in the kernel, and in the microkernel approach, the microkernel will provide a communication between the client programs and it will just help them to communicate with these services which are implemented as system programs and this communication between client programs and system programs is made through with something known as message passing.
- Microkernel can suffer from performance decrease due to the increased system function overhead.
- Only core functionalities are included in the kernel level.
- All other functinalities moved to the system programs.
- Communication between programs use passing message.
![image](https://github.com/user-attachments/assets/9fc6d927-7959-4e24-b8d6-160128ed38b4)
---

##### 5. Module
- One core kernel in the middle have the core kernel functionalities and other functionalities provided as system programs(as in Microkernel).
- Communication between modules through the core kernel(as message passing in Microkernel), so there is no system overhead because the communication done dynamically and directly into the core kernel as and when needed.
- Other functinalities connected to the core kernel.
- Communication between modules through the core kernel.
![image](https://github.com/user-attachments/assets/659568cc-c44c-46ce-8086-3e643f2d0bcd)
---

#### Virtual Machines
##### Understanding the Concept and Functionality of Virtual Machines
- The fundamental idea behind virtual machines is to abstract the hardware of a single computer, including components like the CPU, memory, and network interfaces, into multiple distinct execution environments.
- This abstraction creates the illusion that each environment operates as its own private computer, enabling efficient resource utilization and isolation among various applications running simultaneously on the same physical hardware.

##### Understanding the Structure of Virtual Machines in Computing
- The architecture of a virtual machine involves a physical hardware layer beneath a virtual machine implementation, which facilitates multiple virtual machines.
- Each virtual machine operates its own independent kernel and can run distinct operating systems and processes.
- This setup allows a single physical machine to host several execution environments, enabling better resource management and isolation among different applications running concurrently.

##### Illustrating Multiple Operating Systems on a Single Machine
- In a practical example, a physical machine running a Windows operating system can utilize virtual machine software to create multiple virtual environments.
- Each virtual machine can host different operating systems, such as Linux Mint, various Ubuntu distributions, or Fedora.
- These virtual machines provide the illusion of independent computers, allowing users to operate distinct systems without interference, despite all running on the same physical hardware. This demonstrates the flexibility and efficiency of virtual machine implementations in modern computing.
![image](https://github.com/user-attachments/assets/80e03ac3-b7f2-437d-841a-bee4922b7473)

---
##### Examining User and Kernel Modes in Virtual Machine Operation
- The implementation of virtual machines involves two operational modes: kernel mode and user mode.
- The virtual machine software, which is part of the base operating system, operates in kernel mode, providing essential functionalities and control.
- In contrast, the virtual machines themselves, such as VM1, VM2, and VM3, run in user mode.
- This distinction allows the virtual machines to function independently while leveraging the underlying resources managed by the kernel mode software, illustrating a crucial aspect of virtual machine architecture.

##### Understanding User and Kernel Modes in Virtual Machines
- Virtual machines replicate the operational structure of physical systems by incorporating their own user mode and kernel mode, referred to as virtual user mode and virtual kernel mode. While the virtual machine operates in the physical user mode of the host system, these virtual modes allow for the management of resources and execution of processes within the virtual environment.
- This design enables each virtual machine to function independently, creating the illusion of a private computer for its applications.

##### Benefits of Resource Isolation in Virtual Machine Environments
- Virtual machines provide significant advantages, particularly in resource protection and isolation.
- Each virtual machine operates with its own dedicated resources, preventing interference with others.
- This isolation is achieved by allocating specific disk areas, referred to as mini disks, to each virtual machine, ensuring that the data and resources of one virtual machine are entirely separate from those of another.
- This configuration enhances security and stability, allowing users to run multiple operating systems simultaneously without resource conflicts.

##### Exploring the Installation of Virtual Machines on Your System
- Installing virtual machine software like VMware or VirtualBox allows users to run multiple operating systems concurrently on a single physical machine.
- For instance, a user with a Windows operating system can install Linux Mint within the virtual environment created by the software.
- This setup facilitates seamless switching between the host and guest operating systems, enhancing usability and flexibility for various applications and tasks.
![image](https://github.com/user-attachments/assets/4866bf93-fcd8-4658-a74a-0413ea7fbfd3)
---

#### Operating System Generation & System Boot
##### Operating System Generation
##### Two Approaches to Designing Operating Systems for Machines
- There are two main approaches to designing operating systems:
- The first approach involves creating an operating system tailored for a specific machine at a particular site. This method focuses on the unique requirements of that machine but may not be efficient for broader applications.
- The second approach aims to develop operating systems that can operate across a variety of machines and configurations. This flexibility allows the operating system to function effectively on different hardware, making it a more scalable solution.
##### The Importance of System Generation in Operating Systems
- System generation, often referred to as SYSGEN, is a crucial process that enables an operating system to be tailored for different hardware configurations.
- For instance, an operating system like Linux Mint can be installed on various machines, regardless of their specific hardware differences. This adaptability is achieved through SYSGEN, which configures the operating system to ensure compatibility with the particular machine it is being installed on.
- This method enhances the efficiency and versatility of operating systems, allowing them to function effectively across diverse systems.
##### Key Information Required for System Generation in SYSGEN
- System generation, or SYSGEN, is a process that requires specific information to effectively tailor an operating system for a particular machine.
- The SYSGEN program must identify the CPU type to be used, assess the available memory, determine the connected devices, and understand the desired operating system options.
- This information is crucial as it guides the configuration of the operating system, ensuring it operates efficiently and harmoniously with the machine's hardware and meets user requirements.
![image](https://github.com/user-attachments/assets/8f88a255-1a59-4671-9296-b326b263b60f)
---

##### System Boot
- System bootstrap is the first program to be executed when the computer starts.
- It will locate the OS kernel and load it into the memory to be executed.
- This program is located in the ROM because ROM needs no initialization and safe to computer virus (read-only).
- The OS is located on the disk.
##### Now there is another term that I want to discuss that is called Firmware:
- Firmware is a kind of read-only memory, and in small devices like in your mobile devices, the bootstrap loader or the bootstrap program and the OS both of them reside in the ROM or the firmware. But, the disadvantage of this is that if you want to change something in the ROM then you have to change the entire ROM chip because as we know nothing can be modified.
- But, this problem also has been solved by something known as EPROM which stands for Erasable Programmable Read Only Memory, so this is also a kind of read-only memory in which the contents can only be read. But, by giving an explicit command you can make it writable, so with your consent, it can be made writable.
- So, the kind of firmware, where the bootstrap loader and the operating system both reside in the ROM are used for small devices like mobile devices and all. But, for most of the big computers like desktop computers and laptops, the bootstrap program or the bootstrap loader resides in the ROM, and your main OS resides in the disk.
![image](https://github.com/user-attachments/assets/39e123d3-25d4-4816-9035-e6a75cf9c614)
---

### Process Management 
#### Processes and Threads
##### Understanding the Differences Between Processes and Threads in Operating Systems
- Processes are independent programs in execution that have their own memory space, while threads are smaller units of execution within a process that share the same memory space.
- This distinction is crucial for managing how applications execute and utilize system resources, affecting performance and efficiency in operating systems.
##### The Role of Compilers and Operating Systems in Program Execution
- Compilers are essential tools that convert high-level programming languages into machine code, which consists of binary instructions that computers can understand. However, converting code alone is insufficient for execution; the program must also be loaded into memory. The operating system plays a crucial role in this process, managing the allocation of system resources necessary for the program to run effectively.
##### Understanding the Transition from Program to Process in Computing
- A program is a static entity that exists as code, while a process is defined as the active execution of that program. When a program is loaded into memory and begins execution, it transforms into a process, which can utilize system resources.
- Modern computers support multiple processes running simultaneously, and a single program may have several processes associated with it, highlighting the dynamic nature of program execution in contemporary computing.
##### Defining Threads as the Basic Units of Process Execution
- Threads are the fundamental units of execution within a process, allowing multiple tasks to run concurrently.
- A single process can consist of one or more threads, which execute independently while sharing the same resources. This multi-threading capability enhances performance and efficiency, as it enables better utilization of system resources compared to earlier systems where processes typically contained only a single thread.
![image](https://github.com/user-attachments/assets/9cb39944-f73b-4b43-bdb0-1fe2bb9d2b48)
---

##### Using Task Manager to Monitor Active Processes and Threads
- Task Manager in Windows provides a graphical interface for users to view and manage the processes currently running on their system. By accessing the 'Processes' tab, users can see a list of active programs and their associated threads, enabling them to monitor system performance and resource allocation.
- This tool is essential for identifying resource-intensive applications and managing system workload effectively.
##### Observing Multiple Processes for a Single Application in Task Manager
- In Windows Task Manager, it is common to observe multiple processes associated with a single application, such as the Chrome browser.
- Each instance of chrome.exe represents a separate process, highlighting the application's architecture that utilizes multiple processes for improved performance and stability.
- This capability allows better resource management and isolation between different tasks within the same program, although threads, which run within these processes, may require additional tools like Process Explorer to view.
![image](https://github.com/user-attachments/assets/3c22dd70-a3b6-4006-9cdd-73ee85702304)
---

- If you want to see the threads that are also there in your system, u can use a program known as Process Explorer, you can sownload it and it will show you the threads that are running for each program and for each processes.
![image](https://github.com/user-attachments/assets/7d1c2db8-0149-4e1e-a606-d60cfbadc783)
---

