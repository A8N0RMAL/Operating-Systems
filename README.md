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

## 3. Process Management 

### Processes and Threads
#### Understanding the Differences Between Processes and Threads in Operating Systems
- Processes are independent programs in execution that have their own memory space, while threads are smaller units of execution within a process that share the same memory space.
- This distinction is crucial for managing how applications execute and utilize system resources, affecting performance and efficiency in operating systems.
  
#### The Role of Compilers and Operating Systems in Program Execution
- Compilers are essential tools that convert high-level programming languages into machine code, which consists of binary instructions that computers can understand. However, converting code alone is insufficient for execution; the program must also be loaded into memory. The operating system plays a crucial role in this process, managing the allocation of system resources necessary for the program to run effectively.
  
#### Understanding the Transition from Program to Process in Computing
- A program is a static entity that exists as code, while a process is defined as the active execution of that program. When a program is loaded into memory and begins execution, it transforms into a process, which can utilize system resources.
- Modern computers support multiple processes running simultaneously, and a single program may have several processes associated with it, highlighting the dynamic nature of program execution in contemporary computing.
  
##### Defining Threads as the Basic Units of Process Execution
- Threads are the fundamental units of execution within a process, allowing multiple tasks to run concurrently.
- A single process can consist of one or more threads, which execute independently while sharing the same resources. This multi-threading capability enhances performance and efficiency, as it enables better utilization of system resources compared to earlier systems where processes typically contained only a single thread.
![image](https://github.com/user-attachments/assets/9cb39944-f73b-4b43-bdb0-1fe2bb9d2b48)
---

#### Using Task Manager to Monitor Active Processes and Threads
- Task Manager in Windows provides a graphical interface for users to view and manage the processes currently running on their system. By accessing the 'Processes' tab, users can see a list of active programs and their associated threads, enabling them to monitor system performance and resource allocation.
- This tool is essential for identifying resource-intensive applications and managing system workload effectively.

#### Observing Multiple Processes for a Single Application in Task Manager
- In Windows Task Manager, it is common to observe multiple processes associated with a single application, such as the Chrome browser.
- Each instance of chrome.exe represents a separate process, highlighting the application's architecture that utilizes multiple processes for improved performance and stability.
- This capability allows better resource management and isolation between different tasks within the same program, although threads, which run within these processes, may require additional tools like Process Explorer to view.
![image](https://github.com/user-attachments/assets/3c22dd70-a3b6-4006-9cdd-73ee85702304)
---

- If you want to see the threads that are also there in your system, u can use a program known as Process Explorer, you can sownload it and it will show you the threads that are running for each program and for each processes.
![image](https://github.com/user-attachments/assets/7d1c2db8-0149-4e1e-a606-d60cfbadc783)
---

#### Process State
##### Key States of Process Lifecycle in Operating Systems
- When a process executes, it transitions through various states based on its current activity. The key process states are as follows:
1. New: The process is in the phase of being created.
2. Running: The process's instructions are currently being executed by the processor.
3. Waiting: The process is waiting for an event (e.g., I/O completion, signal reception) to continue execution.
4. Ready: The process is waiting to be assigned to a processor for execution.
5. Terminated: The process has completed its execution and is now finished.
- These states are essential in understanding the lifecycle of a process in an operating system.
![image](https://github.com/user-attachments/assets/46ed0545-6980-4f88-ad5c-c2d57f247129)
---
##### The diagram depicts the lifecycle of a process as it moves through different states:

1. New: The process is being created.
- After being created, the process is admitted to the system and moves to the Ready state.
2. Ready: The process is ready to be executed and is waiting to be assigned to a processor.
- The scheduler dispatches the process from the Ready state to the Running state.
3. Running: Instructions of the process are being executed.
- If the process needs to wait for an event or I/O, it moves to the Waiting state.
- If it gets interrupted, it goes back to the Ready state.
- If the process finishes, it moves to the Terminated state.
4. Waiting: The process is waiting for an event (like I/O) to complete.
- After the event is completed, the process moves back to the Ready state.
5. Terminated: The process has finished execution and exits the system.

##### Key Transitions:
- Admitted: Moves a new process to the Ready state.
- Scheduler Dispatch: Assigns the process to a CPU for execution.
- Interrupt: Causes the process to move back to Ready state from Running.
- I/O or Event Wait: Moves the process from Running to Waiting.
- I/O or Event Completion: Moves the process from Waiting to Ready.
- Exit: Terminates the process after execution is finished.
![image](https://github.com/user-attachments/assets/27e86e0b-201f-48bd-b085-e67045c5b8e6)
---

#### Process Control Block
##### Understanding the Essential Components of a Process Control Block
- Process Control Block(PCB) is used to represent a process in the OS, also called a task control block.
- Each process is represented in the OS by PCB.
- A process control block (PCB) is a critical data structure used by the operating system to manage information about a specific process.
- It contains essential details such as the process state, process number, program counter, registers, and memory limits. These components collectively enable the operating system to track and control the execution of processes efficiently, ensuring that system resources are allocated and managed properly.

##### This block has many parts to control the process
- Process ID (PID) or process number: Unique id of the process, this unique number allows the system to differentiate between processes, ensuring proper management and allocation of resources. By maintaining distinct PIDs, the operating system can track process states, handle scheduling, and facilitate inter-process communication, thus enhancing overall system functionality and efficiency.

- Program Counter (PC): indicates the address of the next instruction to be executed in a running process. As a program executes, the program counter updates to reflect the next line of code, allowing the operating system to track the sequence of execution. This mechanism ensures that instructions are processed in the correct order, facilitating effective program execution and maintaining the overall flow of operations within the system.

- Process State: indicates the current status of a process at any given moment. Processes can exist in various states, including 'New', 'Running', 'Waiting', and 'Terminated', among others. By monitoring the process state, the operating system can effectively manage resource allocation, scheduling, and overall process execution, allowing for efficient multitasking and system performance. The process state serves as a key indicator of a process's activity and facilitates necessary transitions between different operational phases.

- CPU registers: CPU registers are critical components within a process control block (PCB) that store essential information related to the execution of a process. Different types of registers, including index registers, stack pointers, and general-purpose registers, facilitate efficient data handling and instruction execution. By keeping track of these registers, the operating system can effectively manage the state of a process, ensuring that the necessary data is readily available for computations and operations. This management plays a significant role in enhancing overall system performance and responsiveness.

- CPU scheduling : CPU scheduling is an essential function of operating systems that determines the order in which processes are executed. It prioritizes processes based on their urgency and resource requirements, ensuring that higher-priority tasks are executed first. Additionally, scheduling algorithms manage the allocation of CPU time to processes waiting in a queue, optimizing overall system performance. By storing CPU scheduling information in the process control block (PCB), the operating system can make informed decisions about process management, significantly impacting the efficiency of multitasking and responsiveness in a computing environment.

- Memory management: Memory management information is a vital component of a process control block (PCB) that details the memory resources utilized by a specific process. This information encompasses various aspects of memory allocation, such as the amount of memory in use, memory limits, and any memory addresses assigned to the process. By tracking memory management details, the operating system can efficiently allocate resources, prevent memory leaks, and ensure that each process operates within its designated memory space. This functionality is crucial for maintaining overall system stability and performance.

- Accounting information: Accounting information in the Process Control Block (PCB) refers to data that is used to keep track of resource usage for a process. This can include the amount of CPU time consumed, the total execution time, and memory usage. Accounting information is important for tasks such as billing in commercial systems and for system administrators to monitor and control resources efficiently.

- I/O Status information: I/O Status information includes data about the input/output operations related to the process. This may involve information on open files, devices being used by the process, and the status of I/O requests. It ensures that the process can communicate with hardware devices and handle files or streams correctly. This information helps the system manage device assignments and track the completion or pending status of I/O operations.
![image](https://github.com/user-attachments/assets/b88a8d82-e8f7-4003-ad21-72c8099c9eff)
---

#### Process Scheduling
- Objective of multiprogramming: To have multiple processes running simultaneously to maximize CPU utilization. This is important to ensure the CPU is always doing useful work.
- Objective of time-sharing: Time-sharing systems switch the CPU between processes frequently, allowing users to interact with multiple programs efficiently while each is running.
- How process scheduling works: The process scheduler selects an available process for execution from several available processes.
- For single-processor systems, only one process runs at a time.
- For multiple processes, the CPU schedules processes and switches between them. If the CPU is occupied, the remaining processes wait until it becomes available again.
![image](https://github.com/user-attachments/assets/6e744417-1883-4a85-ad33-68c1f0a0c7d2)
---

##### There are 2 types of scheduling queues:
1. Job Queue: This queue holds all processes that are in the system. These processes might be in different stages, waiting to be executed or completed.
2. Ready Queue: This contains processes that are currently in main memory, ready, and waiting to be executed by the CPU. These processes are waiting for CPU time.

##### In the visual representation:
- Processes from the ready queue enter the CPU to get processed.
- After execution, processes may need to perform I/O operations and are sent to the I/O waiting queue.
![image](https://github.com/user-attachments/assets/b65fc316-c694-43ce-85f6-dd1e2704c938)
---

#### What happens to a process when it goes from the ready queue into the running state(when it gets the CPU)
- Swapping: If the process is partially executed and is swapped out of memory (e.g., due to lack of space, process with higher priority comes), it can be swapped back in later to continue its execution.
- I/O Waiting Queue: Processes that are waiting for input or output operations go into the I/O waiting queue. Once the I/O operation is complete, they can be sent back to the ready queue for further CPU execution.
- The diagram shows a process flow: Processes swap in and out of the CPU based on their status. If they're waiting for I/O or need more CPU time, they are placed in the respective queues.
![image](https://github.com/user-attachments/assets/3f1b1a8a-de62-432d-b3c0-1dea2646d030)
---

#### Context Switch
- Definition: Context switching occurs when an interrupt causes the operating system (OS) to stop the CPU's current task and switch to running a kernel routine. This is common in general-purpose systems.
- When one process is suspended and another process is executed due to an interrupt, at that time the context is switched.
##### Process:
1. When an interrupt happens, the OS saves the context (state) of the currently running process.
2. This saved state allows the system to resume the process later from where it was stopped after the interrupt's routine is completed.
3. The context is stored in the Process Control Block (PCB) of the process.
![image](https://github.com/user-attachments/assets/9419f42e-1b59-4c21-a89e-d4969289f9f4)
---
##### Steps Involved:
1. State Save: The system saves the current state (context) of the process running on the CPU.
2. State Restore: After the interrupt routine, the system restores the state of the previously running or new process.

- Overhead: Context-switching time is considered overhead because no useful work is done while the system is switching between processes.
- Performance Factors: The time taken for context switches depends on several factors, such as memory speed, the number of registers, and special instructions for loading or storing registers. Typically, this process takes only a few milliseconds.
![image](https://github.com/user-attachments/assets/e2f3fa72-cef1-45ea-9770-f7b8deaccaa2)
---

#### Operation on Processes – Process Creation
##### Process Creation:
- What is a process? A process is an instance of a program in execution. It can create other processes during its execution using a system call like fork() in Unix/Linux systems.
##### Parent and Child Process:
- The parent process is the one that creates new processes.
- The child process is the new process created by the parent.
- Example: In a Linux system, when you open a terminal and run a command like ls, the terminal (shell) is the parent process. When you type ls, a new process (child process) is created to execute the ls command.
![image](https://github.com/user-attachments/assets/675dcb3d-42b9-451f-9832-271da305bc2b)
---

##### Process Tree:
- The parent process can create multiple children, and these children can also create new processes, forming a tree.
- Example: Consider a system process called init, which starts when the system boots up. It creates processes for handling login (login), network connections (inetd), and more. These in turn create more processes, forming a hierarchical structure, as shown in the process tree.
##### Process Tree on Solaris System:
- The diagram represents a tree of processes in a Solaris operating system. At the root, we have the sched process (PID 0), followed by system processes like init (PID 1).
- Example: The inetd process (which manages network services) creates telnetdaemon, and telnetdaemon creates other processes for specific tasks (e.g., Csh, the C shell). Each of these processes may continue spawning other processes, forming a process hierarchy.
![image](https://github.com/user-attachments/assets/cb4d28b1-7cda-420f-82d2-fc199b032879)

---

##### Process Execution Scenarios:
###### Concurrency between Parent and Child:
- The parent process can continue executing while the child process runs concurrently.
- Example: If you run a background job in Unix/Linux (by appending &), the parent shell will continue to run while the child process (background job) executes.
###### Parent waits for Child Termination:
- The parent process can also wait until its child processes have finished before it continues.
- Example: When you run a command in the foreground, the shell waits for the child process (like cat or grep) to finish before it allows you to input another command.

##### Address Space:
- Two types of child processes in terms of address space:
1. Duplicate of the Parent Process:
- The child process inherits the program and data from the parent process.
- Example: Using fork() in C programming creates a new process with the same code as the parent, but they run independently.

2. New Program Loaded into the Child Process:
- The child process starts executing a new program using a system call like exec().
- Example: After fork(), if the child process calls exec(), it replaces its memory with the new program. A shell might fork() to create a new process, then use exec() to run a new program (e.g., running the ls command).
![image](https://github.com/user-attachments/assets/a5884b83-2e0f-4b93-a070-0cf1414cd08e)
---

#### Operation on Processes – Process Termination
##### Process Termination
- A process ends after executing its final statement and invokes the exit() system call. This signals the operating system to terminate the process.
- Upon termination, the process may return a status value to its parent process using the wait() system call.
- All resources allocated to the process, such as memory, open files, and I/O buffers, are deallocated by the operating system.
![image](https://github.com/user-attachments/assets/ccf7b86c-9813-4775-8066-024b723ecf8a)
---

##### Other Circumstances for Termination:
- One process can terminate another process using an appropriate system call.
- Typically, a parent process can terminate its child process. If this wasn't restricted, users could arbitrarily end each other’s processes.
![image](https://github.com/user-attachments/assets/6c8804ad-43f0-49a3-9123-e51174e6e82c)
---

##### Parent-Child Process Termination:
- A parent process may terminate its child process for several reasons:
1. The child has exceeded its allocated resources.
2. The task assigned to the child is no longer necessary.
3. The parent process is exiting, and in such a case, the operating system doesn't allow the child to continue running.
![image](https://github.com/user-attachments/assets/1acd5744-00d2-49c6-9e1c-79cdb443572c)
---

#### Interprocess Communication
##### Independent vs. Cooperating Processes:
- Independent processes: These processes operate without affecting or being affected by other processes in the system. Each runs in isolation, meaning they don't share data with or depend on other processes.
- Cooperating processes: These processes can be influenced by or can influence other processes. They work together by sharing data and resources, allowing for coordinated execution.
- Example: Web servers and databases are cooperating processes. The web server (Process A) sends a request to the database (Process B) and waits for a response. They cooperate by exchanging data to provide functionality to users.
![image](https://github.com/user-attachments/assets/2433ebc9-3489-4a26-bcca-e69202a0ec95)
---

##### Interprocess Communication which provides an environment, allows process communication. And the reason why we need IPC:
- Information sharing: when several users wants an access to an information it's essential to provide an environment which they can access at the same time. 
- Computation speedup: instead of taking one task at a time, it's better to divide the task to several subtasks which they all work for single task concurrently. In order to achieve this, the subtasks need to communicate each other.
- Modularity: when designing a system, one person will not be designing whole system alone. Therefore, we divide the system to different modules and they'll be put together later on. Also these modules need to cooperate with each other.
- Convenience: from user perspective, if they are utilizing multiple task at a same time meaning different processes are running concurrently. So it'd be convenient if those processes can communicate each other and avoid clashing to one another. 
![image](https://github.com/user-attachments/assets/33b992e4-ce51-4056-892c-2e65f3c2bb0f)
---

##### Models of Inter-process Communication (IPC):
- There are two primary IPC mechanisms:
1. Shared Memory: A region of memory that multiple processes can access and modify. This model allows fast communication since data is directly available for read/write access in memory.
- Example: Processes A and B can both access a common memory space to read or update shared variables.
2. Message Passing: Communication happens through sending and receiving messages between processes. This method is more structured and safer as it doesn’t involve direct memory access.
- Example: Process A sends a message to Process B through a communication channel (like a queue), and Process B receives and processes the message.
![image](https://github.com/user-attachments/assets/4ed57227-df98-440c-843e-1597df180af4)
---

##### Communication Models:
- Shared Memory (Diagram a): Both Process A and Process B use a common memory space labeled as "Shared." They access this shared memory for exchanging information without involving the kernel.
- Message Passing (Diagram b): Process A and Process B communicate by sending messages (indicated by M) through the kernel. The kernel handles message passing, ensuring the two processes can exchange data in a controlled way.
- These concepts are essential for designing systems that involve multiple processes working together or independently, such as multi-threaded applications or distributed systems.
![image](https://github.com/user-attachments/assets/1028aae6-91b7-41ac-abc3-f95c340b487c)
---

#### Shared Memory Systems
- Definition: Interprocess communication (IPC) using shared memory requires that processes establish a common memory region. This region resides in the address space of the process that creates it.

##### How it works:
- One process creates a shared memory segment.
- Other processes must attach this shared memory to their own address space in order to communicate.
- Normally, the OS isolates the memory of different processes to prevent unauthorized access, but shared memory allows multiple processes to bypass this restriction.
- Example: Imagine two processes, Process A and Process B, that need to exchange data. They both attach to the same shared memory space. Process A writes data to the memory, and Process B can read it. For synchronization (to avoid race conditions), mechanisms like mutexes or semaphores are used.
- Mutexes (Mutual Exclusion) and Semaphores are synchronization primitives used in concurrent programming to control access to shared resources, like shared memory, ensuring that processes or threads do not interfere with each other’s operations.

##### Difference between Mutex and Semaphore:
- Mutex: Ensures that only one process/thread can access a resource at a time (one at a time access).
- Semaphore: Can allow multiple processes/threads to access a resource up to a certain limit (can be one or more).

##### Mutex (Mutual Exclusion Object):
- A mutex is a locking mechanism that ensures that only one thread or process can access a shared resource at a time. It is commonly used to prevent race conditions where multiple processes or threads might attempt to access and modify the same data simultaneously.

##### How Mutexes Work:
- A mutex has two states: locked or unlocked.
- A process must lock the mutex before accessing the shared resource.
- If another process tries to lock the mutex while it is already locked, it is forced to wait until the mutex is unlocked (i.e., the other process releases the lock).
- Once the process finishes using the resource, it unlocks the mutex, allowing other waiting processes to proceed.
- Example: Imagine a shared counter in memory that two processes, A and B, want to increment. Without a mutex, both processes might try to increment it at the same time, leading to inconsistent results (race condition). Using a mutex, Process A will lock the counter, increment it, and unlock it, ensuring Process B waits until A finishes.

##### Semaphore:
- A semaphore is a more general synchronization mechanism that can allow access to a shared resource by multiple processes or threads. Semaphores use counters to manage the number of available "permits" to access a resource.

##### There are two types of semaphores:
1. Binary Semaphore: It works like a mutex and has only two values: 0 (locked) and 1 (unlocked).
2. Counting Semaphore: This type of semaphore can have a value greater than 1, allowing multiple processes to access the shared resource simultaneously up to a certain limit.

##### How Semaphores Work:
- A semaphore maintains a count of available resources (or slots).
- A process that wants to access the resource must wait if the count is 0 (indicating all resources are in use). Otherwise, it decreases the count and proceeds.
- When the process is done, it increments the count, signaling that a resource is available for others.
- Example: Imagine a print queue with three printers. If three processes are printing at the same time, the semaphore count will reduce to 0, meaning no more processes can print. If a fourth process attempts to print, it will wait until one printer finishes and the semaphore count increases, indicating an available printer.

##### Example in Context of Shared Memory:
- Mutex Example: Two processes (Producer and Consumer) want to update a shared memory buffer. A mutex can be used to lock the buffer when the Producer writes data to it. The Consumer waits until the Producer unlocks the buffer to read data from it.
- Semaphore Example: In a bounded buffer (e.g., a queue of 5 slots), a counting semaphore can be used to track how many slots are free. If the buffer is full, the Producer waits until the Consumer consumes an item, freeing up a slot. Conversely, another semaphore can track how many items are in the buffer, ensuring the Consumer waits if the buffer is empty.
![image](https://github.com/user-attachments/assets/da9f3bc8-309a-4c19-8c35-159153ff2bba)
---

##### Producer-Consumer Problem:
- Definition: A producer process generates data that is consumed by a consumer process. A common problem in concurrent programming is ensuring that the producer does not produce too much data for the consumer to handle and vice versa.

##### Shared Memory Solution: Shared memory allows the producer and consumer to access a common buffer, where:
- The producer adds items to the buffer.
- The consumer removes items from the buffer.

##### Key Concepts:
- The buffer must be synchronized so that the producer doesn’t overwrite data before it’s consumed, and the consumer doesn’t consume the same item twice.
- Example: Imagine a compiler (producer) that produces assembly code, and an assembler (consumer) that consumes this code to produce object modules. Shared memory acts as the buffer between these processes to facilitate the communication.
![image](https://github.com/user-attachments/assets/f2f6255e-f37b-4067-9ee0-d5ab1ac6884e)
---

##### Types of Buffers in Producer-Consumer Problem:
1. Unbounded Buffer:
- The size of the buffer is theoretically unlimited.
- The consumer may need to wait if no items are available, but the producer can always produce more items without limitation.

2. Bounded Buffer:
- The buffer has a fixed size.
- If the buffer is full, the producer must wait for the consumer to consume items.
- This scenario requires careful synchronization to prevent overfilling and data loss.
- Example: In a bounded buffer, if a producer creates a video stream for a consumer (e.g., a video player), the buffer must manage how much video data is stored at once. If the buffer is full, the producer needs to wait until some of the data is played.
![image](https://github.com/user-attachments/assets/bc01ef36-b8f5-406f-8d8f-e7cbccf45337)
---

#### Message Passing 
- Message passing allows processes to communicate and synchronize their actions without sharing the same memory or address space. This is especially useful in distributed systems, where processes can be on different computers connected via a network.

- Example: Process A and Process B can exchange messages to coordinate without needing to access each other’s memory. These processes rely on a kernel that facilitates the message exchange between them.
- In a distributed setup, processes could reside on different machines, communicating through a network without direct memory access.
![image](https://github.com/user-attachments/assets/d294cda2-6ffa-4b70-bde5-8a285221676f)
---

##### Operations in Message Passing
- Message-passing facilities generally provide two primary operations:
1. Send(message): Allows one process to send a message to another.
2. Receive(message): Allows a process to receive a message from another.

##### Messages can be:
- Fixed Size: Easier to implement but harder for programmers to work with.
- Variable Size: More complex at the system level but simplifies the programming task.

- Example: A client process sending a "request" message to a server process (of fixed or variable size), which the server can then receive and respond to.
![image](https://github.com/user-attachments/assets/65cd16b0-0b90-4d98-bf11-85e49d6528fa)
---

##### Communication Link Between Processes
- For two processes (e.g., Process P and Process Q) to communicate:
- A communication link must be established between them.

##### The system provides various ways to implement this link, supporting different styles of communication:
1. Direct or indirect communication
2. Synchronous or asynchronous communication
3. Buffering (automatic or explicit)

- Example: Process P can send a message to Process Q either directly (via specific identifiers) or indirectly (via a mailbox or channel). They can use either a synchronous method, where both wait for the message transfer, or asynchronous, where they can continue working without waiting for the message to arrive.
![image](https://github.com/user-attachments/assets/59daebfb-3cff-4361-ad0f-1bd6aee5b61e)
---
 
##### Let's discuss the direct and indirect communication and the issue related to them (Naming):
![image](https://github.com/user-attachments/assets/6389698e-0350-4397-8d55-45ec40a996a9)

---

##### Direct Communication
- In a direct communication system, processes explicitly name the sender or recipient.

##### Example:
- send(P, message) sends a message to process P.
- receive(Q, message) receives a message from process Q.

##### Properties:
- A communication link is automatically established between pairs of processes.
- Only two processes can communicate over a link.
- There is symmetry in addressing, meaning both processes must know and name each other to communicate.
![image](https://github.com/user-attachments/assets/3c1850b2-8a33-442a-a1a3-ac5914d0e45a)
---

##### Variant of Direct Communication
- In this variation, only the sender names the recipient. The recipient doesn't need to name the sender.

##### Example:
- send(P, message) sends a message to process P.
- receive(id, message) receives a message from any process, with id indicating the sender's name.

##### Asymmetric Addressing:
- The sender knows the recipient, but the recipient only identifies the sender after receiving the message.
- The disadvantage is limited modularity, meaning if a process's identifier changes, it may require updates to the entire system.
![image](https://github.com/user-attachments/assets/2498d8e6-5bba-41f4-8521-edeffe1c7da2)
---

##### Indirect Communication (Using Mailboxes or Ports)
- In indirect communication, messages are sent and received through shared mailboxes or ports, not between named processes directly.

##### Example:
- send(A, message) sends a message to mailbox A.
- receive(A, message) retrieves a message from mailbox A.

##### Properties:
- Mailboxes are abstract objects that store messages, and processes communicate only if they share a mailbox.
- Each mailbox has a unique ID that processes use to send and receive messages.

##### Conclusion:
- Direct communication requires explicit naming of processes, which may limit flexibility and modularity.
- Indirect communication through mailboxes offers more flexibility, as processes don’t need to know each other but share a common mailbox identifier for communication.
![image](https://github.com/user-attachments/assets/10f10e97-7f76-48f3-8e52-2ce33321c488)
---

##### Message Passing in Operating Systems: Communication Links and Mailboxes
1.  Properties of Communication Links:
- A link is established between two processes only if they both share a mailbox.
- A link can be shared by more than two processes.
- Multiple links can exist between each pair of communicating processes, where each link corresponds to a different mailbox.
![image](https://github.com/user-attachments/assets/cc097062-8f38-4141-9e35-ac7a2e9f113f)
---

2. Message Passing Example (Mailbox A):
- Scenario: Suppose three processes (P1, P2, and P3) share mailbox A. If P1 sends a message to A, both P2 and P3 may attempt to receive the message.

##### Question: Which process (P2 or P3) will receive the message sent by P1?
3. Possible Solutions: The system's behavior will depend on certain factors:
- Restrict Links: If the system restricts the link to be associated with two processes at most, only one receiver (either P2 or P3) will receive the message.
- Single Receive Operation: If only one process can execute a receive() at a time, that process will receive the message.
- Arbitrary Selection: The system can arbitrarily decide which process (P2 or P3) gets the message, possibly using an algorithm like round-robin, where the
processes take turns receiving messages.
- The system might also notify the sender (P1) of which receiver got the message.

4. Ownership of Mailboxes:
- A mailbox can either be owned by a process or managed by the operating system. If the mailbox is owned by a process, it controls how messages are sent and received. If owned by the OS, the system arbitrates message handling.
##### Example:
- Process P1 sends a message to mailbox A: If P2 and P3 both attempt to receive the message, the system decides which process gets it based on one of the factors (e.g., round-robin selection).
- This mechanism ensures flexible and controlled inter-process communication in operating systems using message-passing techniques.
![image](https://github.com/user-attachments/assets/cf9092bc-6bf2-4331-b7b1-9c7dc10b3231)
![image](https://github.com/user-attachments/assets/d0d72bd8-dbba-4400-97e3-fd41eab66145)
---

#### Synchronous or asynchronous communication and synchronization issue related to them:
#### Buffering (automatic or explicit) and buffering issue related to them:
![image](https://github.com/user-attachments/assets/91967325-df08-493c-80cb-a7b061271161)

---

#### Synchronous or asynchronous communication and synchronization issue related to them:
##### Synchronization in Message Passing: 
- Message passing allows processes to communicate by sending and receiving messages. This communication can be either blocking or nonblocking, which are also referred to as synchronous and asynchronous operations.

##### Blocking Send:
- The sending process is halted until the receiving process or the mailbox has received the message.
- Example: If Process A sends a message to Process B, Process A will stop its execution until Process B acknowledges that it has received the message.

##### Nonblocking Send:
- The sender resumes its operation immediately after sending the message, without waiting for it to be received.
- Example: Process A sends a message to Process B and continues with its work, even if Process B hasn’t yet received or processed the message.

##### Blocking Receive:
- The receiving process is suspended until a message becomes available.
- Example: Process B waits and does nothing until it receives a message from Process A.

##### Nonblocking Receive:
- The receiver fetches a message if available, or receives a null if no message is present, allowing it to continue with other tasks.
- Example: Process B checks for messages and continues its work, even if no messages are available.
![image](https://github.com/user-attachments/assets/a543f1e5-d1be-4402-a7be-45364a9f61a0)
---

#### Buffering (automatic or explicit) and buffering issue related to them:
##### Buffering in Message Passing:
- Messages exchanged between processes are stored in temporary queues, which can be implemented in three ways depending on their capacity:

##### Zero Capacity:
- The queue has no space to store messages, meaning the sender must wait until the receiver is ready to receive the message (blocking).
- Example: Process A cannot send a message until Process B is ready to receive it.

##### Bounded Capacity:
- The queue has a limited size, and at most n messages can be stored. If the queue is full, the sender must wait for space to become available.
- Example: Process A sends messages to a queue, but if the queue is full (e.g., 10 messages), Process A must wait until Process B retrieves some messages from the queue.

##### Unbounded Capacity:
- The queue can store an infinite number of messages, so the sender never has to block and can always send messages without waiting.
- Example: Process A keeps sending messages, and the queue dynamically expands to hold all of them without forcing Process A to wait.
![image](https://github.com/user-attachments/assets/20ba02b0-a069-4518-99af-1cd3f81a6eb3)
---

#### Sockets in Operating System
- Sockets are crucial for communication in Client-Server Systems and serve as endpoints for data exchange between processes over a network. Here’s a breakdown of how sockets function:

##### Definition and Identification:
- A socket acts as an endpoint in a network communication link.
- Each socket is identified by a unique combination of an IP address and a port number. This enables communication between a pair of processes, where each process has its own socket.

##### How Socket Communication Works:
- The server process listens on a specified port for incoming client requests.
- Once a client requests a connection, the server accepts it, creating a connection between the client’s socket and the server’s socket.
- Example: A web server might listen on port 80 for HTTP requests. When a client (browser) requests a web page, it connects to the server’s socket at IP address 161.25.19.8 on port 80.

##### Well-Known Ports:
- Specific ports are designated for well-known services:
1. Telnet: Port 23
2. FTP: Port 21
3. HTTP: Port 80
- Example: A telnet server waiting for a connection on port 23 allows clients to connect for remote command-line access.
![image](https://github.com/user-attachments/assets/150476a4-e6cf-4423-ac78-36e4f21c793c)
---

##### Port Numbers and Connection Process:
- Client Process: When a client initiates a connection, it is assigned a random port number (typically above 1024) by the host. This port number, along with the client’s IP address, forms the client’s socket.
- Example: A client with IP 146.86.5.20 initiates a request using port 1625 to connect to a web server socket on IP 161.25.19.8 and port 80.
- Packet Delivery: Data packets sent between the client and server are directed to the correct sockets using IP addresses and port numbers, ensuring they reach the appropriate processes.

##### Common Port Ranges:
- Ports below 1024 are considered well-known and reserved for standard services.
- Ports above 1024 are available for general or custom application use.
![image](https://github.com/user-attachments/assets/7250eff0-6734-4fb0-a51a-da17655593b8)
---

#### Remote Procedure Calls (RPC)
##### What is Remote Procedure Call (RPC)?
- Remote Procedure Call (RPC) is a protocol that allows one program to request a service from a program located on another computer within a network. RPC enables this without the programs needing to understand the details of the network, making it similar in concept to inter-process communication (IPC).

##### Key Concepts and Steps in RPC

1. **Message-Based Communication**:
   - Since the processes run on separate systems, RPC uses a **message-based communication scheme** for requesting and providing remote services. Each communication is structured as a message, rather than simple data packets.

2. **RPC Daemon**:
   - Each message is directed to an **RPC daemon** on the remote system, which listens to a specific port. The message includes:
     - An identifier for the function to be executed.
     - Any parameters needed for the function.

3. **Execution and Response**:
   - Once the request is received, the function is executed as requested, and the output is sent back to the requester through another message.
![image](https://github.com/user-attachments/assets/15a17854-ea97-4d5d-83a8-1a714f08c4e7)
---

##### Semantic Details in RPC
- RPC allows a client to invoke a procedure on a remote server as if it were a local call. Here’s how it works:

1. **Client-Side Stub**:
   - RPC hides the details of the network communication by using a **stub** on the client side. This stub acts as a placeholder for each remote procedure.

2. **Remote Procedure Invocation**:
   - When a client calls a remote procedure, the RPC system invokes the appropriate stub, passing the provided parameters. 
   - The stub finds the server’s port and prepares (marshals) the parameters for network transmission.

3. **Parameter Marshalling**:
   - Parameters are **marshalled** by converting them into a format suitable for network transmission. This ensures they can be understood by the server, regardless of network differences.

4. **Message Passing**:
   - The client stub then sends a message to the server using message passing. On the server side, a corresponding stub receives this message and executes the procedure on the server.

5. **Returning Values**:
   - If necessary, the server’s output (return value) is packaged and sent back to the client in the same way.

#### Example Scenario
- Imagine a file storage system where a client application wants to retrieve a file from a remote server.
1. The client application calls a function like `getFile("example.txt")`.
2. The RPC stub on the client marshals the `getFile` function and `"example.txt"` parameter, then sends this as a message to the server.
3. The server’s stub receives this message, unpacks it, and calls `getFile("example.txt")` on the server.
4. The server executes the request, retrieves the file data, and sends it back to the client through a response message.
5. The client’s stub receives the response, unmarshals the data, and presents it as if it were a local call.

#### Advantages of RPC
- **Transparency**: RPC hides network details, making remote functions appear local.
- **Efficiency**: It uses message-passing for streamlined communication between distributed systems.
- **Structure**: Communication is well-defined and organized, making it suitable for structured network applications. 

- This setup simplifies network-based program interactions, enabling efficient, scalable services across distributed systems.
![image](https://github.com/user-attachments/assets/57d2d5a7-7778-4b28-9587-9dc64838456a)
---

#### Issues in RPC & How They're Resolved
1) Difference in representation of data in different systems. Can be solved by using a machine-independent representation of data. Practical example is XDR(eXternal Data Representation)
2) Network issues can make redundant calls or cause a failure of the procedure execution. Can be solved by ensuring that the OS executes the procedure exactly once not at most once.
3) RPCs requires that the client knows the server's port address where the RPC daemon is running on. This can be solved by agreeing on a fixed port numbers for communication, or dynamically finding out the port address using the rendezvous mechanism.

#### Let's dig in deep with more details:
#### 1. Data Representation Differences
- **Issue**: Different systems (client and server) may represent data differently, such as big-endian and little-endian formats for storing 32-bit integers. Big-endian systems store the most significant byte at the highest memory address, while little-endian systems do the opposite.
- **Solution**: RPC systems use a machine-independent representation called External Data Representation (XDR). When data is sent, it’s converted to XDR format on the client side, ensuring a standardized format across different machines. On the server side, the data is unmarshalled and converted back to the server’s native format.

#### 2. Failure and Duplication in RPCs
- **Issue**: Unlike local procedure calls, RPCs can fail or duplicate calls due to network errors, causing them to be executed multiple times unintentionally.
- **Solution**: The operating system ensures that messages are processed exactly once, though achieving this is more challenging than the "at most once" approach that some systems employ. This ensures RPC reliability by preventing duplicated executions.
![image](https://github.com/user-attachments/assets/210bc505-9f14-4639-be12-f81eb2f429fb)
---

#### 3. Binding of Client and Server Ports
- **Issue**: In standard procedure calls, binding occurs during link, load, or execution time. However, RPC requires binding the client to the server's port, which is complicated as neither system has full information about the other’s resources.
- **Solution**:
  - **Fixed Port Addresses**: A predetermined port is assigned to the RPC during compile time, allowing the client to know the server's port address.
  - **Rendezvous Mechanism**: An operating system daemon, known as a matchmaker, dynamically provides the port information to the client when requested. This daemon assigns the correct port for the RPC call, maintaining flexibility for the server.
![image-fotor-20241030171835](https://github.com/user-attachments/assets/11870fb0-e24e-450d-a90d-69b596799a02)
---

#### 4. Execution of RPC (Process Flow)
- **Process**:
  - The client requests a procedure call.
  - The operating system looks up the port via a matchmaker and returns the correct port.
  - The client then sends the request to the specified port.
  - The server daemon processes the request and sends back the output.

- This structured flow ensures that RPC calls are directed to the right endpoints and managed effectively to maintain the procedure's integrity. This process minimizes the typical network-related issues by establishing reliable communication paths. 
![image](https://github.com/user-attachments/assets/201d3e01-1969-4c43-b114-0a5387988d72)
---

## 3.2 Threads

### What is a Thread?
- A **thread** is the smallest unit of CPU execution.
- Each thread contains:
  - **Thread ID**: Unique identifier for the thread.
  - **Program Counter**: Tracks the current instruction.
  - **Register Set**: Holds the state of the processor.
  - **Stack**: Stores the thread’s local variables and method calls.

#### Threads within the same process share:
- **Code section**, **data section**, and **open files**.
- **Operating system resources** such as memory.

### Single-Threaded vs. Multi-Threaded Processes
- **Single-threaded process**: Contains only one thread of control.
- **Multi-threaded process**: Contains multiple threads, allowing multiple tasks to execute concurrently.

**Example**: 
  - In a text editor, one thread might handle user input while another handles spell-checking in the background. This improves responsiveness and allows tasks to run concurrently.
![image](https://github.com/user-attachments/assets/0e033347-55de-48ff-8ecf-0ce91ff2b3c6)
---

### Benefits of Multithreading
- Multithreading brings multiple advantages that fall into four main categories:

1. **Responsiveness**:
   - Keeps an application running even if one thread is blocked or performing a long operation.
   - **Example**: In a web browser, one thread can handle user inputs while another loads content in the background.

2. **Resource Sharing**:
   - Threads share memory and resources within the same address space.
   - **Example**: Multiple threads in a photo editing app can access the same image data without needing separate memory allocations, saving resources.

3. **Economy**:
   - Creating and managing threads is cheaper than creating new processes because threads share resources of the parent process.
   - **Example**: In a server application, multiple threads can handle client requests without needing the overhead of creating a new process for each request.

4. **Utilization of Multiprocessor Architectures**:
   - Threads can run in parallel on multiple processors, increasing efficiency.
   - **Example**: A video rendering program can split tasks among multiple CPU cores to speed up the process.

![image](https://github.com/user-attachments/assets/ae9c56a8-ecbc-466a-81a0-b3e3ed06482d)

---

### Multithreading Models & Hyperthreading

### Types of Threads
1. **User Threads**: These are managed by a thread library in user space without direct kernel support.
2. **Kernel Threads**: Managed by the operating system (OS) kernel.

#### The relationship between user threads and kernel threads is established through three main multithreading models:
![image](https://github.com/user-attachments/assets/270d2541-2702-4622-88a2-007ac35625ff)

---

### 1. **Many-to-One Model**
   - **Description**: Maps multiple user threads to a single kernel thread.
   - **Benefits**: Efficient thread management in user space.
   - **Drawbacks**: If one thread makes a blocking system call, the entire process is blocked. Also, multiple threads cannot run in parallel on multiprocessors.
   - **Example**: Some older threading libraries, such as Java's green threads, use this model, where all user threads are mapped onto a single kernel thread, limiting concurrent execution.
![image](https://github.com/user-attachments/assets/267c13a9-ac53-4d5b-a40a-b715f550f3d8)
---

### 2. **One-to-One Model**
   - **Description**: Maps each user thread to a separate kernel thread.
   - **Benefits**: Provides higher concurrency since threads can run in parallel on multiprocessors.
   - **Drawbacks**: The creation of each user thread requires a kernel thread, which can be resource-intensive. Many implementations restrict the maximum number of threads due to overhead.
   - **Example**: POSIX Threads (Pthreads) on Linux are often implemented using a one-to-one model, where each user thread directly corresponds to a kernel thread, allowing for high levels of concurrency.
![image](https://github.com/user-attachments/assets/a254295d-e60e-40e0-89ed-7a02ab192f7d)
---

### 3. **Many-to-Many Model**
   - **Description**: Allows multiple user threads to be mapped to an equal or smaller number of kernel threads.
   - **Benefits**: Provides flexibility in thread creation, as the OS can schedule user threads more effectively based on system resources.
   - **Drawbacks**: Complex implementation due to the need for synchronization between user and kernel threads.
   - **Example**: Windows’ fiber system allows multiple fibers (user threads) to be executed across available kernel threads, making it an example of a many-to-many model.
![image](https://github.com/user-attachments/assets/1f3e9cdf-30d0-4063-8104-856e01ccf346)
---

### Hyperthreading (Simultaneous Multithreading or SMT)
   - **Description**: A technique where a single physical processor core appears as multiple logical processors to the OS. This allows each core to execute multiple threads simultaneously, improving performance by efficiently utilizing processor resources.
   - **Example**: Intel's Hyper-Threading Technology (HTT) enables a core to handle two threads simultaneously. In the example command output provided (`wmic CPU Get NumberOfCores, NumberOfLogicalProcessors`), a CPU with six cores and twelve logical processors demonstrates hyperthreading, where each core has two logical processors.

- These concepts optimize the way an OS handles concurrent processes, leading to more efficient use of CPU resources in multitasking environments. Hyperthreading, for instance, can be beneficial in workloads with high CPU usage, such as video rendering or large-scale data analysis.
![image](https://github.com/user-attachments/assets/8f2f78f2-78da-48ab-8d13-28406e8da7b4)
![image](https://github.com/user-attachments/assets/6f509bdd-2947-4623-87fa-5e50de8880e2)
---

### `fork()` and `exec()` System Calls in Linux

1. **`fork()`**:
   - The `fork()` system call is used to create a new process by duplicating the calling process. 
   - When `fork()` is called, it creates a **separate, duplicate process** that is identical to the parent, including its code, data, and open files.
   - The new process created by `fork()` is known as the "child" process, and it runs independently of the "parent" process.
   - Example:
![image](https://github.com/user-attachments/assets/29313a72-34e9-495d-bded-39836a80897e)


2. **`exec()`**:
   - The `exec()` system call replaces the current process with a new program specified in its parameters.
   - When `exec()` is invoked, the calling process's code, data, and stack are replaced with the new program, including all threads.
   - This means the new program runs in place of the calling process, with the same process ID, but all previous memory and resources are replaced.
   - Example:
![image](https://github.com/user-attachments/assets/87166323-4340-4387-b745-026988b4802d)


- In summary, `fork()` is used to create a duplicate process, while `exec()` replaces the current process with a different program. They are often used together, with `fork()` creating a new process and `exec()` running a new program within that process.
![image](https://github.com/user-attachments/assets/21f5a5e8-e99f-4b0c-94a2-14b107a4b5c8)
---

### Threading Issues with `fork()` and `exec()` Calls in Multithreaded Programs
- In a multithreaded environment, the behavior of the `fork()` and `exec()` system calls can introduce challenges, especially around duplicating threads and managing process execution. 
![image](https://github.com/user-attachments/assets/966e91ec-a062-4932-8613-d5a7177e153f)
![image](https://github.com/user-attachments/assets/d7636c7b-57d1-4d68-b742-7f1d463a5ae1)
---

#### The `fork()` System Call in Multithreaded Programs

- **Issue**:
  When a thread within a multithreaded program calls `fork()`, there’s ambiguity about whether the new process should duplicate all threads in the original process or only the thread that called `fork()`.

- **Solution**:
  Some UNIX systems offer two versions of `fork()`:
    - One version duplicates **all threads** from the original process.
    - Another version duplicates **only the thread** that invoked `fork()`, creating a new process with a single thread.

- **Choosing Which Version**:
  Deciding which version of `fork()` to use depends on the behavior needed in the program after `fork()` is called.

---

#### The `exec()` System Call in Multithreaded Programs

- If a thread calls `exec()` after `fork()`, the `exec()` system call will replace the entire process image (including all threads) with a new program as specified. This makes it unnecessary to duplicate all threads when `exec()` will immediately follow `fork()`.

---

### Guidelines for Using `fork()` and `exec()` Together

- The choice of `fork()` behavior depends on whether `exec()` is invoked immediately after `fork()` or not:

1. **If `exec()` is called immediately after `fork()`**:
   - **Duplicate only the calling thread**: Duplicating all threads would be wasteful because `exec()` replaces the process image, so any additional threads created would immediately be discarded.
   - Example:
![image](https://github.com/user-attachments/assets/c317a3f0-2b05-423c-a725-d12cb2ff0f29)


2. **If `exec()` is NOT called after `fork()`**:
   - **Duplicate all threads**: If the separate process created by `fork()` is expected to continue execution without calling `exec()`, then it should duplicate all threads to maintain the same multithreaded context as the parent process.

---

### Summary

- **When to duplicate only the calling thread**: Use this version if `exec()` will follow `fork()` immediately, as it avoids creating extra threads that will be discarded.
- **When to duplicate all threads**: Use this if the new process created by `fork()` will not call `exec()` and is expected to maintain the same multithreaded environment as the parent.

- These considerations are essential for optimizing resource usage and ensuring correct behavior when using `fork()` and `exec()` in multithreaded programs.

---

### Threading Issues (Thread Cancellation)
- Thread cancellation is the process of stopping a thread before it completes its task. It is typically done in cases where the result is already obtained by one thread, or the task has been canceled by the user. 

**Examples:**
1. **Database Search:** Multiple threads are searching a database. Once one thread finds the desired result, the remaining threads are canceled to save resources.
2. **Web Browsing:** If a user stops a webpage from loading, all threads responsible for loading that page are canceled.
![image](https://github.com/user-attachments/assets/4b0df3e8-82f3-48bc-b517-3405e2caf8e8)

---

### Types of Thread Cancellation
- There are two primary ways to cancel a thread:

1. **Asynchronous Cancellation:**  
   - A thread is terminated immediately by another thread.
   - **Example:** Pressing a "Stop" button in a web browser to halt all loading threads instantly.

2. **Deferred Cancellation:**  
   - The target thread periodically checks if it should terminate, allowing it to finish important tasks or free resources safely.
   - **Example:** A thread processing data checks at intervals if it should be canceled, preventing issues like memory leaks.
![image](https://github.com/user-attachments/assets/f98a4e15-1cc7-4eec-ba8a-7ff7cee3bf7b)

---

### Challenges with Thread Cancellation
Thread cancellation can be problematic in certain situations, particularly when:
- **Resources are allocated to the canceled thread.**
- **The thread is actively sharing data with others.**

- If a thread is canceled abruptly, not all resources may be freed, potentially causing resource leakage. The Operating System reclaims some resources, but system-wide resources may remain occupied.

**Deferred Cancellation** helps manage these issues by allowing threads to reach a safe point for termination:
- **Example:** Before canceling, a thread can check if it’s safe to terminate, ensuring that no essential resources are locked or left unused.
![image](https://github.com/user-attachments/assets/31a7193f-09ca-4915-98af-56e08f3dde84)

---

## 3.3 CPU Scheduling

#### **What is CPU Scheduling?**
- CPU scheduling is essential for **multiprogrammed operating systems**.
- It helps in switching the CPU among different processes, increasing the overall productivity of the system.

#### **Key Topics Covered**:
1. Introduction to CPU scheduling.
2. Overview of various CPU scheduling algorithms.
![image](https://github.com/user-attachments/assets/7dac8d2e-5177-4214-a03d-04c8be957dbe)

---

### **Single-Processor System:**
- **Limitation**: Only one process can run at a time; others must wait until the CPU is free.
- **Idle Time Problem**:
  - When a process waits for I/O (Input/Output), the CPU sits idle, leading to wasted time.

#### **Objective of Multiprogramming**:
- Keep the CPU as busy as possible by ensuring there’s always a process ready to run.
- **Goal**: Maximize CPU utilization by:
  1. Running a process continuously.
  2. Switching to another process if the current one is waiting (e.g., for an I/O request).
![image](https://github.com/user-attachments/assets/e78e1514-e614-4f50-87d1-3017cb853549)

---

### **Benefits of Multiprogramming:**
- Keeps multiple processes in memory simultaneously.
- When one process is idle (e.g., waiting for I/O), the CPU is assigned to another process.

#### **Practical Example**:
- Suppose a system has:
  1. **Process A** performing calculations (CPU-intensive).
  2. **Process B** waiting for a file to load (I/O).
  
- If the CPU runs **only Process A**, Process B must wait unnecessarily. Multiprogramming allows Process B to run while Process A is idle during its I/O wait.
![image](https://github.com/user-attachments/assets/c7c5bdbd-6442-4359-96fc-6d08d6a6d7be)
---

### **CPU and I/O Burst Cycles**

#### **Key Concepts**:
1. **Process Execution Cycle**:
   - A process alternates between two states during its execution:
     - **CPU Burst**: Time spent by the process performing computations in the CPU.
     - **I/O Burst**: Time spent waiting for Input/Output operations (e.g., reading/writing data).

2. **Cycle Explanation**:
   - Process execution starts with a **CPU burst**.
   - This is followed by an **I/O burst**.
   - This alternating pattern continues: **CPU burst → I/O burst → CPU burst**, and so on.
   - Eventually, a **final CPU burst** completes the process, often ending with a system request for termination.

#### **Definitions**:
- **CPU Burst**: The phase where the CPU actively executes instructions of the process.
  - Example: Performing arithmetic computations, updating variables in memory.
- **I/O Burst**: The phase where the CPU waits for I/O operations to complete.
  - Example: Waiting for data to be read from or written to a file.
![image](https://github.com/user-attachments/assets/f7532350-2615-4e08-8994-dbce34443f99)

---

### **Example of Alternating Bursts**:
#### Workflow from the Image:
1. **First CPU Burst**:
   - Operations: `load`, `store`, `add`, `read from file`.
2. **I/O Burst**:
   - Waiting for I/O to read or write data.
3. **Second CPU Burst**:
   - Operations: `store`, `increment`, `index`, `write to file`.
4. **Next I/O Burst**:
   - Waiting for file operations to complete.
5. **Further Alternations**:
   - The process continues alternating between **CPU bursts** and **I/O bursts** until the final CPU burst finishes.
![image](https://github.com/user-attachments/assets/7b2481df-0caa-4d23-a062-43f07e27f54b)

---

### **Example in Practice**:
Consider a process handling a large dataset:
1. **CPU Burst**:
   - Perform calculations on a portion of the data.
2. **I/O Burst**:
   - Wait for the next portion of the data to be loaded from the hard drive.
3. **Repeat**:
   - Continue alternating as the CPU processes each chunk and waits for the next.

- This alternating pattern optimizes resource usage by ensuring the CPU works while I/O operations are being prepared in parallel.

### Real-World Example
- A program processing a dataset:
   - **CPU Burst**: Process the current chunk of data.
   - **I/O Burst**: Load the next chunk from disk.

---

### **Preemptive and Non-Preemptive Scheduling**

#### Key Concepts:
1. **CPU Scheduler**:
   - Selects processes from the **ready queue** when the CPU is idle.
   - Assigns the CPU to one of these processes using the **short-term scheduler**.

2. **Dispatcher**:
   - Hands control of the CPU to the selected process.
   - Responsible for switching context, loading process states, etc.
   - **Dispatch Latency**: The time it takes to stop one process and start another.
![image](https://github.com/user-attachments/assets/c5a26e24-63c1-4477-90b5-720bb62f1ac5)

---

### Scheduling Scenarios:
Scheduling decisions occur during:
1. **Switch from Running to Waiting state**:
   - Example: A process requires I/O operations.

2. **Switch from Running to Ready state**:
   - Example: An interrupt occurs (e.g., a higher-priority process preempts the current one).

3. **Switch from Waiting to Ready state**:
   - Example: Completion of an I/O operation signals the process is ready.

4. **Process Termination**:
   - Example: The process completes its execution and exits.
![image](https://github.com/user-attachments/assets/019d1eaa-8b17-479d-b48d-af9c1f2708bd)

---

#### Preemptive Scheduling:
- **Definition**: The CPU can be taken away from the current running process if a higher-priority process arrives.
- **Examples**:
  - **Round Robin (RR)**: Each process gets a fixed time slice; the CPU is preempted after the slice expires.
  - **Priority Scheduling** (Preemptive): A higher-priority process interrupts a lower-priority one.
- **Scenario**: Applies to cases **2** and **3** where the CPU is preempted based on priority or time quantum.

---

#### Non-Preemptive Scheduling:
- **Definition**: Once the CPU is assigned to a process, it cannot be preempted until the process completes or moves to a waiting state.
- **Examples**:
  - **First-Come, First-Served (FCFS)**: Processes are executed in the order they arrive.
  - **Priority Scheduling** (Non-Preemptive): Lower-priority processes continue execution until completion, regardless of new arrivals.
- **Scenario**: Applies to cases **1** and **4**, where the CPU is only reassigned after process termination or an I/O request.

---

#### Example Comparisons:
1. **Preemptive**:
   - Process A is running; Process B (higher priority) arrives.
   - The CPU is preempted, and Process B starts executing.

2. **Non-Preemptive**:
   - Process A is running; Process B (higher priority) arrives.
   - Process A finishes, then Process B begins.
---

### **Scheduling Criteria**
- Scheduling criteria in an operating system are used to evaluate the efficiency of CPU scheduling algorithms. These criteria include:

---

### **1. CPU Utilization**
- **Definition**: The percentage of time the CPU is actively working (executing processes) as opposed to being idle.
- **Range**: 
  - Real systems typically aim for 40% (lightly loaded system) to 90% (heavily loaded system).
- **Goal**: Keep the CPU as busy as possible.
  
**Example**:  
If the CPU is idle for 2 seconds out of every 10 seconds, the CPU utilization is `80%`.

---

### **2. Throughput**
- **Definition**: The number of processes completed per unit of time.
- **Goal**: Maximize the number of processes completed.

**Example**:  
If 5 processes are completed in 1 second, the throughput is `5` processes/second.

---

### **3. Turnaround Time**
- **Definition**: The total time taken from the submission of a process to its completion.
- **Formula**:  
  **Turnaround Time** = `Waiting Time` + `Execution Time` + `I/O Time`
- **Goal**: Minimize turnaround time for processes.

**Example**:  
- Process A is submitted at time 0.
- It waits for 2 seconds in the queue, executes for 3 seconds, and performs I/O for 1 second.  
**Turnaround time** = `2 + 3 + 1 = 6` seconds.
![Screenshot 2024-11-19 192955](https://github.com/user-attachments/assets/2680bd19-69ad-42d1-a4b8-f975fb1fe424)

---

### **4. Waiting Time**
- **Definition**: The total time a process spends waiting in the ready queue before getting executed.
- **Goal**: Reduce waiting time.

**Example**:  
If a process waits for `3` seconds before its execution starts, its waiting time is `3` seconds.

---

### **5. Response Time**
- **Definition**: The time interval between the submission of a process and the generation of the first response (output).
- **Goal**: Minimize response time, especially in interactive systems.
  
**Example**:  
- A user requests data at time 0.
- The system generates the first response at time 2.  
Response time =  `2` seconds.
![Screenshot 2024-11-19 193005](https://github.com/user-attachments/assets/3fec7cc9-3a39-4b9c-8112-d0a3e8fad2fe)

---

**Key Notes**:
- **Turnaround time** is important for batch systems where the overall completion time matters.  
- **Response time** is more critical in interactive systems to ensure the system feels responsive to the user.  
- Different scheduling algorithms prioritize these criteria differently depending on system goals (e.g., Round Robin for better response time, First-Come-First-Serve for simplicity).

---

### First-Come, First-Served (FCFS) Scheduling Algorithm

#### **Overview**
- **FCFS** is the simplest CPU scheduling algorithm.
- Processes are scheduled in the order they arrive (First-In, First-Out, FIFO).
- Once a process enters the ready queue, its Process Control Block (PCB) is added to the end of the queue.
- When the CPU is free, it is allocated to the process at the front of the queue, and the process runs until completion.

#### **Characteristics**
- **Non-preemptive**: Once the CPU is allocated, the process holds it until termination or I/O request.
- Easy to implement but not ideal for systems requiring regular CPU access for all users.
![Screenshot 2024-11-20 185920](https://github.com/user-attachments/assets/3019d1f4-11d0-48bd-b85f-deda8c9fa43b)

---

#### **Example**
Consider three processes with their **burst times** as shown:

| Process | Burst Time (ms) |
|---------|-----------------|
| P1      | 24              |
| P2      | 3               |
| P3      | 3               |

**Case 1**: Arrival Order = P1 → P2 → P3  
Gantt Chart:  
```
P1 | P2 | P3
  0   24   27   30
```

- **Waiting Time**:  
  - P1 = 0 ms  
  - P2 = 24 ms  
  - P3 = 27 ms  
- **Average Waiting Time**:  
  `frac(0 + 24 + 27) / 3 = 17 ms`

---

**Case 2**: Arrival Order = P2 → P3 → P1  
Gantt Chart:  
```
P2 | P3 | P1
  0    3    6    30
```

- **Waiting Time**:  
  - P2 = 0 ms  
  - P3 = 3 ms  
  - P1 = 6 ms  
- **Average Waiting Time**:  
  `frac (0 + 3 + 6) / 3 = 3  ms`
![image](https://github.com/user-attachments/assets/4e8018d8-6a32-43d6-9d10-ccde55b16caf)

---

#### **Observations**
- **Order Matters**: The waiting time varies significantly based on the arrival order of processes.
- **Drawback**: Processes with long burst times can delay others (convoy effect), leading to poor average waiting times.
![image](https://github.com/user-attachments/assets/2953d97e-e396-4a08-a4fe-2666947f705d)

---

#### **Use Cases**
- Suitable for batch processing where process arrival order doesn't change.
- Inefficient for time-sharing systems where equal CPU time is necessary for all users.  
---

#### **What is FCFS Scheduling?**
- **FCFS** is the simplest CPU scheduling algorithm where the process that arrives first gets executed first.
- It's a non-preemptive algorithm, meaning once a process starts execution, it runs to completion.
- Processes are scheduled in the order they arrive in the ready queue.

---

#### **Key Term: Convoy Effect**
- **Convoy Effect** occurs when processes with a **longer burst time** are scheduled before processes with a **shorter burst time**.
- This forces smaller processes to wait, causing inefficiency in CPU utilization.
![image](https://github.com/user-attachments/assets/4c6b1895-0d80-441f-9a2c-9105116b4462)

Example:  
If a process with a burst time of 10 units arrives first and smaller processes with burst times of 2 and 1 units arrive later, the CPU remains occupied with the larger process while the smaller ones wait.

---

#### **Example Problem**
Consider the following **5 processes** with their **arrival times** and **burst times**:

| Process ID | Arrival Time | Burst Time |
|------------|--------------|------------|
| P1         | 4            | 5          |
| P2         | 6            | 4          |
| P3         | 0            | 3          |
| P4         | 6            | 2          |
| P5         | 5            | 4          |

##### Step 1: Gantt Chart Construction
- The Gantt Chart shows the order of process execution:

- The **shaded box** represents CPU idle time (no process is available).

##### Step 2: Calculating Times for Each Process
- **Turnaround Time (TAT)** = Completion Time - Arrival Time  
- **Waiting Time (WT)** = Turnaround Time - Burst Time

| Process ID | Completion Time | Turnaround Time | Waiting Time |
|------------|-----------------|-----------------|--------------|
| P1         | 9               | 9 - 4 = 5       | 5 - 5 = 0    |
| P2         | 17              | 17 - 6 = 11     | 11 - 4 = 7   |
| P3         | 3               | 3 - 0 = 3       | 3 - 3 = 0    |
| P4         | 19              | 19 - 6 = 13     | 13 - 2 = 11  |
| P5         | 13              | 13 - 5 = 8      | 8 - 4 = 4    |

##### Step 3: Average Turnaround and Waiting Time
![image](https://github.com/user-attachments/assets/a5676e96-114b-48a9-b564-db9ef7cc4f13)

---

#### **Key Observations**
1. **Idle Time**:
   - CPU remains idle from time 3 to 4, as no process is available at that moment.
2. **Convoy Effect**:
   - The longer process P1 delays smaller processes P5 and P4 , increasing their waiting times.

---

#### **Advantages of FCFS**:
- Simple and easy to implement.
- Processes are executed in the exact order of their arrival.

#### **Disadvantages of FCFS**:
- **Convoy Effect** reduces efficiency and increases the average waiting time.
- Not suitable for time-sharing systems or interactive processes.

---

## First-Come, First-Served (FCFS) Scheduling

**Problem Statement**:  
We are given a set of processes, their arrival times, and their burst times (execution times). Using the **FCFS scheduling algorithm**:
1. Processes are executed in the order they arrive.
2. One unit of overhead is added while scheduling each process.
3. The task is to calculate the **efficiency** of the algorithm.
![Screenshot 2024-11-23 171023](https://github.com/user-attachments/assets/56237fbd-bd63-433b-9c3c-357aa878c7fa)

---

### Example:

| Process ID | Arrival Time | Burst Time |
|------------|--------------|------------|
| P1         | 0            | 3          |
| P2         | 1            | 2          |
| P3         | 2            | 1          |
| P4         | 3            | 4          |
| P5         | 4            | 5          |
| P6         | 5            | 2          |

- **Overhead per process**: 1 unit.

---

### Gantt Chart

The Gantt chart illustrates the execution order and duration of each process, including the overhead (denoted as δ):
![Screenshot 2024-11-23 171040](https://github.com/user-attachments/assets/45949ef5-1bc9-4d54-ae65-ab7fc2b49287)

---

### Calculation of Wasted and Useful Time

1. **Wasted Time**:  
   Wasted time is caused by the overhead introduced while scheduling processes.  
   - Wasted Time = Number of Processes times Overhead per process
   `Wasted Time = 6 times 1 = 6 units`

2. **Total Time**:  
   - Total time is the duration from the start to the end of the last process.  
   `Total Time = 23 units`

3. **Useful Time**:  
   Useful time is the total time spent executing the processes (excluding the overhead).  
  
   `Useful Time = Total Time - Wasted Time`
   `Useful Time = 23 - 6 = 17 units`

---

### Efficiency Calculation

Efficiency `eta` is the ratio of useful time to total time:  

`eta = Useful Time \ Total Time`
`eta = 17 \ 23 approx 0.7391 or 73.91%`
![Screenshot 2024-11-23 171051](https://github.com/user-attachments/assets/ff7bb975-2bd7-4d1c-98a3-29c4b2980f6d)

---

### Final Notes

1. **Efficiency**: The scheduling efficiency is `73.91% `. The remaining `26.09%` is wasted due to scheduling overhead.
2. **Key Characteristics of FCFS**:
   - Processes are scheduled in the order they arrive.
   - Simple but non-preemptive (a process cannot be interrupted once started).
   - Wasted time due to overhead impacts efficiency as the number of processes grows.
---

### **Shortest Job First (SJF) Scheduling Algorithm**
SJF is a CPU scheduling algorithm that assigns the CPU to processes based on the shortest next CPU burst. 

- **Key Features:**
  - The process with the smallest next CPU burst is selected first.
  - If two processes have the same burst length, **First-Come-First-Serve (FCFS)** is used to break ties.
  - SJF can be **preemptive** or **non-preemptive**:
    - **Non-preemptive SJF**: Once a process starts execution, it cannot be stopped until it finishes.
    - **Preemptive SJF**: Also called **Shortest Remaining Time First (SRTF)**, where a process may be preempted if a new process with a shorter burst arrives.
  - It is sometimes referred to as the **Shortest-Next-CPU-Burst Algorithm**, emphasizing its focus on the immediate next CPU burst length.
![Screenshot 2024-11-24 174214](https://github.com/user-attachments/assets/c2e33bf3-b898-4bfc-931e-d8cafd8b3477)

---

### **Example 1: Non-Preemptive SJF**
**Processes:**

| Process ID | Burst Time |
|------------|------------|
| P1         | 6          |
| P2         | 8          |
| P3         | 7          |
| P4         | 3          |

**Execution:**
- The process with the shortest burst time (P4) runs first, followed by P1, P3, and finally P2.

**Waiting Times:**
-  P1 = 3 
-  P2 = 16 
-  P3 = 9 
-  P4 = 0 

**Average Waiting Time:**  
`(3 + 16 + 9 + 0) / 4 = 7 ms` 

*Comparison with FCFS:* In FCFS, the average waiting time would have been **10.25 ms**, highlighting SJF’s efficiency.
![Screenshot 2024-11-24 174225](https://github.com/user-attachments/assets/b8f28074-fd11-43ea-bb74-d30b30dd03ba)

---

### **Example 2: Preemptive SJF (SRTF)**
**Processes:**

| Process ID | Arrival Time | Burst Time |
|------------|--------------|------------|
| P1         | 0            | 7          |
| P2         | 1            | 4          |
| P3         | 2            | 9          |
| P4         | 3            | 5          |

**Waiting Times:**
-  `P1 = 9`  
-  `P2 = 0`
-  `P3 = 15`  
-  `P4 = 2`

**Average Waiting Time:**  
`(9 + 0 + 15 + 2) / 4 = 6.5 ms`
![Screenshot 2024-11-24 174242](https://github.com/user-attachments/assets/bd68d8b3-70c4-4091-8d62-f4cc083f1d88)

---

### **Problems with SJF Scheduling**
1. **Difficulty in Knowing CPU Burst Lengths:**
   - Predicting the exact length of the next CPU burst is challenging, as the algorithm requires prior knowledge of the CPU burst times.

2. **Optimality vs. Practicality:**
   - Although SJF minimizes average waiting time, it is often not feasible to implement in real-world systems.

3. **Approximations:**
   - To overcome this limitation, past CPU burst times can be used to estimate the next burst length. Processes with shorter predicted CPU bursts are prioritized.
![Screenshot 2024-11-24 174255](https://github.com/user-attachments/assets/9a7a07b6-649b-4b80-8de0-7a4acdbc97ed)

---

### Shortest Job First (SJF) Scheduling Explanation and Example

**Definition**:  
Shortest Job First (SJF) is a CPU scheduling algorithm where the process with the shortest burst time is executed first. If two processes have the same burst time, they are scheduled based on their arrival time. It can operate in two modes:
- **Non-preemptive**: Once a process starts execution, it cannot be stopped until it's completed.
- **Preemptive** (also known as Shortest Remaining Time First, SRTF): The CPU can be taken from the currently executing process if a new process arrives with a shorter burst time.
![Screenshot 2024-11-25 182746](https://github.com/user-attachments/assets/80358af6-0a44-48b2-b386-685c34535cee)

---

### Problem Summary

We are solving a problem where **preemptive SJF scheduling** (Shortest Remaining Time First) is applied. The goal is to calculate the **average waiting time** for the given processes.

#### Input Table
| Process ID | Arrival Time (ms) | Burst Time (ms) |
|------------|--------------------|-----------------|
| P1         | 0                 | 12              |
| P2         | 2                 | 4               |
| P3         | 3                 | 6               |
| P4         | 8                 | 5               |

---

### Steps to Solve

1. **Construct a Gantt Chart**:  
   Allocate CPU time based on the shortest remaining burst time among all arrived processes.

   | Time Interval | Executing Process |
   |---------------|-------------------|
   | 0 - 2         | P1                |
   | 2 - 6         | P2                |
   | 6 - 12        | P3                |
   | 12 - 17       | P4                |
   | 17 - 27       | P1                |

2. **Calculate Waiting Time for Each Process**:
   - **Waiting Time Formula**:  
     `Waiting Time = Completion Time - Arrival Time - Burst Time`

   | Process | Completion Time (ms) | Arrival Time (ms) | Burst Time (ms) | Waiting Time (ms) |
   |---------|-----------------------|-------------------|-----------------|-------------------|
   | P1      | 27                    | 0                 | 12              | \( 27 - 0 - 12 = 15 \) |
   | P2      | 6                     | 2                 | 4               | \( 6 - 2 - 4 = 0 \)  |
   | P3      | 12                    | 3                 | 6               | \( 12 - 3 - 6 = 3 \) |
   | P4      | 17                    | 8                 | 5               | \( 17 - 8 - 5 = 4 \) |

3. **Calculate Average Waiting Time**:
   - Total Waiting Time: `15 + 0 + 3 + 4 = 22`
   - Average Waiting Time:  `{Total Waiting Time} / {Number of Processes} = 22 / 4 = 5.5 ms`

---

### Example Output
**Gantt Chart Representation**:  
`0(P1)2(P2)6(P3)12(P4)17(P1)27`

**Average Waiting Time**: `5.5 ms`
![Screenshot 2024-11-25 182800](https://github.com/user-attachments/assets/78eb35af-4188-47f2-af74-b26527d98cc0)

---

### Key Notes:
- SJF minimizes **average waiting time**, making it optimal for batch processing.
- In **preemptive SJF**, processes can be interrupted, leading to dynamic changes in CPU allocation based on new arrivals.
---


### Shortest Job First (SJF) Scheduling: Preemptive (Shortest Remaining Time First)

#### Problem Overview
- **Processes**: Each process has an **arrival time** and a **burst time** (execution duration).
- **Goal**: Minimize the average turnaround time by selecting the process with the shortest remaining burst time at every scheduling step.

#### Example Problem:
| **Process ID** | **Arrival Time** | **Burst Time** |
|-----------------|------------------|----------------|
| P1              | 0                | 10             |
| P2              | 3                | 6              |
| P3              | 7                | 1              |
| P4              | 8                | 3              |

- **Scheduling Type**: Preemptive SJF (Shortest Remaining Time First).
![Screenshot 2024-11-26 160324](https://github.com/user-attachments/assets/6cc97a8d-31ab-4214-8d77-338b96c90b16)

---

### Solution Steps:
#### 1. **Gantt Chart Construction**:
   - A Gantt chart represents the timeline and which process is executed at each moment.

   | Time Intervals | Process Executed |
   |----------------|------------------|
   | 0 to 3         | P1               |
   | 3 to 7         | P2               |
   | 7 to 8         | P3               |
   | 8 to 10        | P2               |
   | 10 to 13       | P4               |
   | 13 to 20       | P1               |

   **Final Gantt Chart**:  
   ```
   | P1 | P2 | P3 | P2 | P4 | P1 |
   0    3    7    8    10   13   20
   ```

---

#### 2. **Turnaround Time Calculation**:
   - **Turnaround Time (TAT)**:  
     TAT = Completion Time - Arrival Time

   **Completion Times**:  
   - P1: 20, P2: 10, P3: 8, P4: 13  

   **Turnaround Times**:
   - **P1**: `20 - 0 = 20`
   - **P2**: `10 - 3 = 7`
   - **P3**: `8 - 7 = 1`
   - **P4**: `13 - 8 = 5`

---

#### 3. **Average Turnaround Time**:
   - **Formula**:  
     `Average TAT = Sum of TATs / Number of Processes`
   - `Average TAT = (20 + 7 + 1 + 5) / 4 = 33 / 4 = 8.25 ms`
![Screenshot 2024-11-26 160334](https://github.com/user-attachments/assets/01556bb4-a481-4f63-ac8f-c5933ea3492f)

---

### Key Takeaways:
1. **Preemptive SJF Scheduling** ensures the shortest burst time process gets priority, even if a new process arrives mid-execution.
2. The **average turnaround time** is minimized, making this approach efficient for real-time systems.
---


### Priority Scheduling

#### 1. **Introduction**
- **Definition:** In Priority Scheduling, a priority is associated with each process, and the CPU is allocated to the process with the highest priority.
  - **Higher priority → Executed first.**
  - Equal-priority processes are scheduled in **First-Come-First-Served (FCFS)** order.
- **Special Case:** Shortest Job First (SJF) is a type of Priority Scheduling where the priority is determined by the next CPU burst (smaller bursts = higher priority).

#### 2. **Types of Priority Scheduling**
- **Preemptive Priority Scheduling:**  
  - A higher-priority process can interrupt the currently running process.
- **Non-Preemptive Priority Scheduling:**  
  - A higher-priority process is added to the ready queue and executed after the current process finishes.
![Screenshot 2024-11-27 183355](https://github.com/user-attachments/assets/e60042fc-636a-4bc7-94e8-f9ccf71fb2a4)

---

#### 3. **Example Problem**

**Processes:**
| Process ID | Burst Time | Priority |
|------------|------------|----------|
| P1         | 10 ms      | 3        |
| P2         | 1 ms       | 1        |
| P3         | 2 ms       | 4        |
| P4         | 1 ms       | 5        |
| P5         | 5 ms       | 2        |

**Scheduling Order (Higher priority = Lower number):**  
**P2 → P5 → P1 → P3 → P4**

**Waiting Times:**  
- P1: 6 ms  
- P2: 0 ms  
- P3: 16 ms  
- P4: 18 ms  
- P5: 1 ms  

**Average Waiting Time:**  
`Average Waiting Time = (6 + 0 + 16 + 18 + 1)/ 5 = 8.2 ms`
![Screenshot 2024-11-27 183405](https://github.com/user-attachments/assets/b5375b2c-ee80-4562-a5bc-b1fe984fe0dd)

---

#### 4. **Problems with Priority Scheduling**
- **Starvation (Indefinite Blocking):**  
  - Low-priority processes might never execute if higher-priority processes keep arriving.

---

#### 5. **Solution to Starvation: Aging**
- Gradually increase the priority of a process as it waits in the ready queue.
  - Example: Increment priority by 1 every 15 minutes.
  - This ensures that even initially low-priority processes eventually execute.
![Screenshot 2024-11-27 183413](https://github.com/user-attachments/assets/f5269dff-4ebb-4689-b717-d6066824ceb4)

---

### **Priority Scheduling (Preemptive)**

#### Problem:
We are given a set of processes with their **arrival time**, **burst time**, and **priority**. In this example, **priority 0 is the highest**. The task is to calculate the **average waiting time** using the preemptive priority scheduling algorithm.
![Screenshot 2024-11-28 145849](https://github.com/user-attachments/assets/7b3a83cd-1378-4e7e-9369-03bc056e0ee7)

---

#### **Processes Information**:

| Process ID | Arrival Time (ms) | Burst Time (ms) | Priority |
|------------|--------------------|-----------------|----------|
| P1         | 0                 | 11              | 2        |
| P2         | 5                 | 28              | 0        |
| P3         | 12                | 2               | 3        |
| P4         | 2                 | 10              | 1        |
| P5         | 9                 | 16              | 4        |

---

#### **Steps to Solve**:

1. **Gantt Chart Construction**:
   The scheduling is done by selecting the process with the **highest priority** (lowest priority number) among the processes that have arrived.

   **Gantt Chart**:

   - From **0 to 2 ms**: P1 executes (priority = 2).
   - At **2 ms**, P4 (priority = 1) preempts P1.
   - At **5 ms**, P2 (priority = 0) arrives and preempts P4.
   - Once P2 finishes at **33 ms**, P1 resumes and completes at **40 ms**.
   - At **40 ms**, P3 executes (priority = 3) and completes at **49 ms**.
   - Finally, P5 (priority = 4) executes from **49 ms** to **67 ms**.
![Screenshot 2024-11-28 145900](https://github.com/user-attachments/assets/eec5ed69-7a7d-4e33-b9e1-01d0f19c953c)

---

#### **Calculating Waiting Time**:

- **Waiting Time Formula**:
  `Waiting Time = Start Time - Arrival Time`

| Process | Completion Time | Arrival Time | Burst Time | Waiting Time |
|---------|-----------------|--------------|------------|--------------|
| P1      | 40              | 0            | 11         | `( 40 - 11 - 0 = 38 ) ms` |
| P2      | 33              | 5            | 28         | `( 33 - 28 - 5 = 0 ) ms` |
| P3      | 49              | 12           | 2          | `( 49 - 12 - 2 = 37 ) ms` |
| P4      | 33              | 2            | 10         | `( 33 - 10 - 2 = 28 ) ms` |
| P5      | 67              | 9            | 16         | `( 67 - 16 - 9 = 42 ) ms` |

---

#### **Average Waiting Time**:
`Average Waiting Time = Sum of Waiting Times / Number of Processes`
 `(38 + 0 + 37 + 28 + 42) / 5 = 145 / 5 = 29 ms`

---

### **Key Points**:
- **Preemptive Priority Scheduling** allows higher-priority processes to interrupt lower-priority ones.
- The **waiting time** is calculated by factoring in when the process starts and its arrival.
- This scheduling favors **high-priority processes** but may lead to **starvation** for lower-priority ones.

---

### **Priority Scheduling (Non-Preemptive) Example**

#### Problem:
Given a set of processes with their **Arrival Time**, **Burst Time**, and **Priority**, determine:
1. **Average Waiting Time**
2. **Average Turnaround Time**

The **Higher number represents higher priority**, and the scheduling policy is **non-preemptive**, meaning a process in execution cannot be interrupted by another.
![Screenshot 2024-11-30 172123](https://github.com/user-attachments/assets/dafae3c3-46a0-4a89-9902-61fff279a525)

#### Input Data:
| Process ID | Arrival Time | Burst Time | Priority |
|------------|--------------|------------|----------|
| P1         | 0            | 4          | 2        |
| P2         | 1            | 3          | 3        |
| P3         | 2            | 1          | 4        |
| P4         | 3            | 5          | 5        |
| P5         | 4            | 2          | 5        |

---

### **Solution**

1. **Determine Execution Order (Gantt Chart)**:
   - At time `0`, P1 starts as it is the only available process.
   - After P1 finishes, prioritize higher-priority processes that have arrived by then.
   - The execution order (Gantt chart):

2. **Completion Time**:
   Completion Time is the time a process finishes execution. From the Gantt chart:
   - P1 = 4 ms
   - P4 = 9 ms
   - P5 = 11 ms
   - P3 = 12 ms
   - P2 = 15 ms

3. **Turnaround Time (TAT)**:
   TAT = Completion Time - Arrival Time
   - P1 = 4 - 0 = 4 ms
   - P2 = 15 - 1 = 14 ms
   - P3 = 12 - 2 = 10 ms
   - P4 = 9 - 3 = 6 ms
   - P5 = 11 - 4 = 7 ms

4. **Waiting Time (WT)**:
   WT = Turnaround Time - Burst Time
   - P1 = 4 - 4 = 0 ms
   - P2 = 14 - 3 = 11 ms
   - P3 = 10 - 1 = 9 ms
   - P4 = 6 - 5 = 1 ms
   - P5 = 7 - 2 = 5 ms

---

### **Final Results**
- **Average Turnaround Time (TAT)**:
  `Average TAT = (4 + 14 + 10 + 6 + 7) / 5 = 41 / 5 = 8.2 ms`

- **Average Waiting Time (WT)**:
  `Average WT = (0 + 11 + 9 + 1 + 5) / 5 = 26/ 5 = 5.2 ms`
![Screenshot 2024-11-30 172026](https://github.com/user-attachments/assets/23b27794-4429-4327-92a8-6ede640879b6)

---


### **Round Robin Scheduling**
- **Overview**: 
  - This algorithm is designed for time-sharing systems.
  - It is similar to First-Come, First-Served (FCFS) scheduling but introduces **preemption** using a fixed time slice or quantum.
  - The ready queue is treated as a **circular queue**.
  
- **Key Features**:
  - Each process is given a specific amount of time (time quantum) to execute.
  - If the process doesn’t finish in its time quantum, it is preempted and added back to the end of the queue.
  - The CPU scheduler continues to allocate CPU to processes in a **round-robin manner**.
![Screenshot 2024-12-01 162755](https://github.com/user-attachments/assets/07f691df-c1b2-4c69-9974-e5043f2ba400)

---

### **Implementation of Round Robin**
1. **Ready Queue as FIFO**:
   - The queue operates on a **First In, First Out** principle.
   - New processes are added to the tail of the queue.
   - The CPU scheduler picks the first process from the queue.

2. **Process Execution**:
   - The CPU sets a timer for 1 time quantum and begins executing the process.
   - After the time quantum expires, **one of two scenarios** occurs:
     1. **Scenario 1**: If the process completes within the time quantum:
        - The process releases the CPU voluntarily.
        - The scheduler moves to the next process in the queue.
     2. **Scenario 2**: If the process's burst time exceeds the time quantum:
        - A **context switch** occurs.
        - The process is preempted and moved to the **tail of the ready queue**.
        - The scheduler moves to the next process.
![Screenshot 2024-12-01 163441](https://github.com/user-attachments/assets/382075e0-618a-4ab7-8395-f77d4db4dcda)

---

### **Benefits of Round Robin**:
- **Fair Allocation**: Ensures that every process gets a chance to execute within the time quantum.
- **Responsive for Interactive Systems**: Well-suited for systems with many users or interactive tasks.
  
### **Challenges**:
- **Time Quantum Selection**:
  - Too small → Increased context switching overhead.
  - Too large → Behaves like FCFS.

---

**Round Robin Scheduling (Turnaround Time and Waiting Time)**
- Round Robin (RR) Scheduling is a preemptive CPU scheduling algorithm. It allocates the CPU to each process in a cyclic order, with a fixed "time quantum" or "time slice."
![Screenshot 2024-12-02 145833](https://github.com/user-attachments/assets/69fd7dea-71b6-409e-a9e6-a29eb28c2ad0)

---

**Given Problem Details:**
- **Processes**: P1, P2, P3
- **Burst Times**: 
  - P1: 24 ms
  - P2: 3 ms
  - P3: 3 ms
- **Time Quantum**: 4 ms

---

### **Execution Process:**
1. **Gantt Chart**: 
   The CPU executes each process for a maximum of 4 ms (time quantum) or until its burst time is fully completed. 

   - P1 executes for 4 ms and is preempted as it still has 20 ms remaining.
   - P2 and P3 each execute for their full burst times (3 ms each) as their burst times are less than the time quantum.
   - P1 continues executing in chunks of 4 ms until its burst time is completed at time 30 ms.
![Screenshot 2024-12-02 150359](https://github.com/user-attachments/assets/e0db0cd3-ca68-40ae-b53c-3a65beb0b28a)

---

### **Key Metrics:**

#### **Turnaround Time (TAT)**:
   Formula:  
   `TAT = Completion Time - Arrival Time`
   - P1: ( 30 - 0 ) = 30  ms
   - P2: ( 7 - 0 ) = 7  ms
   - P3: ( 10 - 0 ) = 10  ms

   **Average TAT**:
   30 + 7 + 10 / 3 = 15.66 ms

---

#### **Waiting Time (WT)**:
   **Method 1**:  
   `WT = TAT - Burst Time`
   
   - P1: ( 30 - 24 ) = 6 ms
   - P2: ( 7 - 3 ) = 4  ms
   - P3: ( 10 - 3 ) = 7  ms

   **Method 2**:  
   Using the formula:  
   `WT = Last Start Time - Arrival Time - (Preemptions * Time Quantum)`
   
   - P1: ( 26 - 0 - (5 * 4)) = 6  ms
   - P2: ( 4 - 0 - (0 * 4)) = 4  ms
   - P3: ( 7 - 0 - (0 * 4)) = 7  ms

   **Average WT**:
   6 + 4 + 7 / 3 = 5.66 ms
![Screenshot 2024-12-02 150529](https://github.com/user-attachments/assets/38990138-8df2-4027-9262-8a820bdacdf7)

---

### **Summary Table:**

| Process ID | Completion Time | Turnaround Time (TAT) | Waiting Time (WT) |
|------------|-----------------|-----------------------|-------------------|
| P1         | 30              | 30                    | 6                 |
| P2         | 7               | 7                     | 4                 |
| P3         | 10              | 10                    | 7                 |

---

### **Conclusion**:
Round Robin ensures fairness by giving each process an equal time slice. However, the performance depends on the chosen time quantum:
- A small time quantum increases context switching overhead.
- A large time quantum may cause longer waiting times for shorter processes. 
---


### Round Robin Scheduling with Solved Problem

#### Problem Setup
- **Processes**: A set of 5 processes with their arrival times and burst times:
  | Process ID | Arrival Time | Burst Time |
  |------------|--------------|------------|
  | P1         | 0            | 5          |
  | P2         | 1            | 3          |
  | P3         | 2            | 1          |
  | P4         | 3            | 2          |
  | P5         | 4            | 3          |

- **Time Quantum**: 2 units.
- **Objective**: Calculate the average waiting time and average turnaround time.
![Screenshot 2024-12-03 164821](https://github.com/user-attachments/assets/78e4b5cb-3416-4715-97ab-e2f14b78bf17)

---

#### Gantt Chart
The processes are executed in a cyclic order, following the time quantum of 2 units. The execution proceeds as follows:

| Time | Process Executed |
|------|-------------------|
| 0-2  | P1               |
| 2-4  | P2               |
| 4-5  | P3               |
| 5-7  | P1               |
| 7-9  | P4               |
| 9-11 | P5               |
| 11-12| P2               |
| 12-13| P1               |
| 13-14| P5               |
![Screenshot 2024-12-03 170011](https://github.com/user-attachments/assets/83a9bdd0-d900-4aa3-931d-4c3f17a6915e)

---

#### Calculations

1. **Completion Time (CT)**:
   The time at which a process finishes execution.
   - P1: 13, P2: 12, P3: 5, P4: 9, P5: 14.

2. **Turnaround Time (TAT)**:
   `TAT = Completion Time - Arrival Time`
   - P1: ( 13 - 0 = 13 )
   - P2: ( 12 - 1 = 11 )
   - P3: ( 5 - 2 = 3 )
   - P4: ( 9 - 3 = 6 )
   - P5: ( 14 - 4 = 10 )

   **Average TAT**:
   `Avg TAT = (13 + 11 + 3 + 6 + 10) / 5 = 8.6 units`

3. **Waiting Time (WT)**:
   `WT = TAT - Burst Time`
   - P1: ( 13 - 5 = 8 )
   - P2: ( 11 - 3 = 8 )
   - P3: ( 3 - 1 = 2 )
   - P4: ( 6 - 2 = 4 )
   - P5: ( 10 - 3 = 7 )

   **Average WT**:
   `Avg WT = (8 + 8 + 2 + 4 + 7) / 5 = 5.8 units`
![Screenshot 2024-12-03 170705](https://github.com/user-attachments/assets/7cffd8da-0d87-46e2-9a4d-205617c7da12)

---

### Key Notes:
- **Round Robin Scheduling** ensures fairness by allotting each process a fixed time quantum in cyclic order.
- It minimizes response time but may increase waiting and turnaround times compared to other algorithms.

---


### **Multilevel Queue Scheduling**
This scheduling algorithm is designed for situations where processes can be grouped into categories based on specific characteristics (e.g., type or priority). Each group is assigned its own queue, and processes are permanently assigned to one queue based on attributes like:
- Memory size
- Process priority
- Process type (e.g., interactive or batch)
![Screenshot 2024-12-04 193649](https://github.com/user-attachments/assets/c3ada249-4833-4041-a7e5-024aa8c27250)

---

### **Key Concepts**
1. **Separate Queues**:
   - Processes are classified into **foreground (interactive)** and **background (batch)** processes.
   - Each queue may have different scheduling requirements and uses a unique scheduling algorithm.

2. **Examples of Queue Scheduling**:
   - **Foreground Queue**: Uses **Round Robin (RR)** for quick response.
   - **Background Queue**: Uses **First-Come, First-Served (FCFS)** for simplicity.
   - **Inter-Queue Scheduling**: Often uses **Fixed-Priority Preemptive Scheduling**, where the foreground queue has absolute priority over the background queue.

3. **Practical Application**:
   - System processes get the highest priority.
   - Student processes or other low-priority jobs are placed at the lowest level.
![Screenshot 2024-12-04 194046](https://github.com/user-attachments/assets/f2d3a599-1dc3-4622-b416-86fc4bb0cf50)

---

### **Example of Queues in Order of Priority**
(From highest to lowest):
1. **System Processes**  
2. **Interactive Processes**  
3. **Interactive Editing Processes**  
4. **Batch Processes**  
5. **Student Processes**

This prioritization ensures that critical tasks are completed before less important ones.

---

### **Advantages**
- Better resource allocation based on process type.
- Customizable scheduling for each queue based on requirements.

### **Disadvantages**
- Starvation can occur for low-priority processes if high-priority queues dominate CPU time.
![Screenshot 2024-12-04 200220](https://github.com/user-attachments/assets/3212bfcd-af19-4cce-9648-80c8bf16427e)
---


### **Multilevel Feedback-Queue Scheduling**
This algorithm allows processes to move between queues based on their behavior and CPU burst characteristics. It provides flexibility to optimize CPU utilization and prevents issues like starvation.

#### **Key Points:**
1. **Dynamic Priority Adjustment:**
   - Processes are separated into queues based on their CPU burst characteristics.
   - If a process uses excessive CPU time, it is moved to a lower-priority queue.
   - **Example:** A CPU-bound process initially in a higher-priority queue might get downgraded if it frequently exceeds its time quantum.

2. **Favoring I/O-Bound Processes:**
   - Interactive and I/O-bound processes are kept in higher-priority queues since they often require minimal CPU time and interact frequently with the user.
   - **Example:** A text editor's process would stay in a higher-priority queue to ensure responsiveness.

3. **Aging to Prevent Starvation:**
   - A process waiting too long in a lower-priority queue can be promoted to a higher-priority queue.
   - This mechanism ensures no process is indefinitely delayed.
   - **Example:** A background task in a lower-priority queue might be promoted after a specified waiting time to avoid neglect.
![Screenshot 2024-12-05 161932](https://github.com/user-attachments/assets/5f2a46b1-5e1b-45d3-a633-eefddf5fcac7)

---

### **Structure of Queues**
The structure typically involves multiple queues, each with a different scheduling strategy or time quantum.

- **Queue 0:** Highest priority, smallest time quantum (e.g., 8 ms).
- **Queue 1:** Medium priority, larger time quantum (e.g., 16 ms).
- **Queue 2:** Lowest priority, typically managed using First-Come, First-Served (FCFS) scheduling.

#### **Process Movement Between Queues:**
- A new process starts in the highest-priority queue.
- If it exhausts its time quantum without completion, it is demoted to a lower-priority queue.
- **Example:** A process begins in Queue 0 (time quantum = 8 ms). If it doesn’t finish within 8 ms, it moves to Queue 1 (time quantum = 16 ms).
![Screenshot 2024-12-05 162321](https://github.com/user-attachments/assets/3c9f0caa-269e-4bd2-8b59-3686b60070b6)

---

### **Parameters of Multilevel Feedback-Queue Scheduling**
The algorithm is defined by several parameters that determine its behavior:

1. **Number of Queues:**
   - Defines how processes are grouped.
   - **Example:** Three queues as shown in the figure.

2. **Scheduling Algorithm for Each Queue:**
   - Determines how processes within a queue are scheduled.
   - **Example:** Queue 0 uses Round Robin with a time quantum of 8 ms, while Queue 2 uses FCFS.

3. **Upgrade/Demote Methods:**
   - Rules for promoting or demoting processes between queues based on their execution behavior.
   - **Example:** Promote a process if it has waited longer than a predefined threshold.

4. **Queue Entry Method:**
   - Defines which queue a process enters when it needs service.
   - **Example:** A newly created process enters the highest-priority queue.
![Screenshot 2024-12-05 162831](https://github.com/user-attachments/assets/506182d6-55ef-477b-81f1-2672f5141ba4)

---

## Scheduling Algorithms (Solved Problems)
## Question 1: Maximum Throughput in Scheduling Algorithms (GATE 2001)

### Problem:
Consider a set of n tasks with known runtimes ( r1, r2, ..., rn ) to be run on a uniprocessor machine. Which of the following processor scheduling algorithms will result in the maximum throughput?

1. (a) Round-Robin
2. (b) Highest-Response-Ratio-Next
3. (c) Shortest-Job-First
4. (d) First-Come-First-Served

### Solution: **(c) Shortest-Job-First**

#### Explanation:
Shortest-Job-First (SJF) prioritizes tasks with the shortest execution time first. By minimizing the average waiting and turnaround time, the algorithm maximizes the number of processes completed within a given time (throughput). Other algorithms like Round-Robin or First-Come-First-Served may not be as efficient for throughput because they do not account for the length of tasks.
![Screenshot 2024-12-07 172133](https://github.com/user-attachments/assets/9e53da7a-4fc0-4c0e-811c-fd2430e9b063)

---

## Question 2: Non-Preemptive Scheduling Algorithm (GATE 2002)

### Problem:
Which of the following scheduling algorithms is non-preemptive?

1. (a) Round-Robin
2. (b) First-In-First-Out
3. (c) Multilevel Queue Scheduling
4. (d) Multilevel Queue Scheduling with Feedback

### Solution: **(b) First-In-First-Out**

#### Explanation:
First-In-First-Out (FIFO), also known as First-Come-First-Served (FCFS), is inherently non-preemptive. Once a process starts execution, it runs to completion without interruption. In contrast, algorithms like Round-Robin and Multilevel Queue Scheduling involve preemption to ensure fairness or priority adjustments.
![Screenshot 2024-12-07 172145](https://github.com/user-attachments/assets/e96e6650-13d5-49ab-83b2-60b71a4c910d)

---

## Question 3: True Statements About Scheduling (GATE 2010)

### Problem:
Which of the following statements are true?

1. **I**: Shortest remaining time first scheduling may cause starvation.
2. **II**: Preemptive scheduling may cause starvation.
3. **III**: Round-Robin is better than FCFS in terms of response time.

1. (a) I only
2. (b) I and III only
3. (c) II and III only
4. (d) I, II, and III

### Solution: **(d) I, II, and III**

#### Explanation:
- **Statement I**: Shortest Remaining Time First (SRTF), a preemptive version of SJF, prioritizes processes with the least time remaining. Long processes can be indefinitely delayed if shorter processes keep arriving, leading to starvation.
- **Statement II**: Preemptive scheduling, such as Priority Scheduling, can also cause starvation if lower-priority processes are repeatedly preempted by higher-priority ones.
- **Statement III**: Round-Robin scheduling improves response time because it ensures that each process gets a time slice regularly, unlike FCFS where a long-running process can delay others.
![Screenshot 2024-12-07 172212](https://github.com/user-attachments/assets/cdfa7d35-31c6-48e2-9c6f-c59cb4ba613b)

---

## Question 4: Process Completion Order in FCFS and RR2 (GATE 2012)

### Problem:
Consider the following processes:

| Process ID | Arrival Time | Time Units Required |
|------------|--------------|---------------------|
| P1         | 0            | 5                  |
| P2         | 1            | 7                  |
| P3         | 3            | 4                  |

The completion order of the processes under the policies FCFS and RR2 (Round Robin with CPU quantum of 2) are:

1. (a) FCFS: P1, P2, P3; RR2: P1, P3, P2
2. (b) FCFS: P1, P3, P2; RR2: P1, P3, P2
3. (c) FCFS: P1, P2, P3; RR2: P1, P2, P3
4. (d) FCFS: P1, P3, P2; RR2: P1, P2, P3

### Solution: **(a) FCFS: P1, P2, P3; RR2: P1, P3, P2**

#### Explanation:
- **FCFS**: Processes are scheduled in the order of their arrival. Hence, P1 runs first, followed by P2, and finally P3.
- **RR2**: With a quantum of 2 time units:
  - P1 executes for 2 units, then P2 for 2 units, followed by P3 for 2 units.
  - P1 resumes for 3 remaining units, then P3 finishes its 2 remaining units, and finally, P2 completes its 3 remaining units.
![Screenshot 2024-12-07 172234](https://github.com/user-attachments/assets/8fb313d9-9a4f-400d-bdf7-bfad99b23844)

---

## Question 5: Algorithm Equivalence (GATE 2013)

### Problem:
A scheduling algorithm assigns priority proportional to the waiting time of a process. The scheduler re-evaluates priorities every ( T ) time units and decides the next process to schedule. Which one of the following is true if the processes have no I/O operations and all arrive at time zero?

1. (a) Equivalent to First-Come-First-Serve
2. (b) Equivalent to Round-Robin
3. (c) Equivalent to Shortest-Job-First
4. (d) Equivalent to Shortest-Remaining-Time-First

### Solution: **(b) Equivalent to Round-Robin**

#### Explanation:
Re-evaluating priorities at fixed intervals ( T ) is characteristic of Round-Robin scheduling. Processes are given equal opportunity to execute, and waiting times increase uniformly, causing priority to rotate cyclically.
![Screenshot 2024-12-07 172248](https://github.com/user-attachments/assets/f40cfddb-a3d0-44ae-8019-203371fcdbc1)

---

### Additional Notes:
- **SJF vs FCFS**: SJF minimizes average waiting time but can cause starvation. FCFS is simple but can lead to poor response time.
- **Round-Robin**: Balances fairness and responsiveness but can have higher average turnaround time.
- **Starvation**: Occurs in priority-based algorithms if low-priority tasks are perpetually delayed by high-priority tasks.
---


## Process Synchronization
### **What is Process Synchronization?**
- **Definition**: Ensures the orderly execution of cooperating processes that share resources or data, preventing issues like *data inconsistency*.
- **Cooperating Processes**: Processes that can share:
  1. Logical address space (code and data).
  2. Files or messages.

Without synchronization, concurrent access to shared data can lead to **race conditions**.
![Screenshot 2024-12-08 200338](https://github.com/user-attachments/assets/8d4d8057-535d-434c-a028-878c169e9cef)

---

### **Key Problem: Producer-Consumer Problem**
The producer-consumer problem is a classic example of process synchronization where:
- **Producer**: Produces data (e.g., items) into a buffer.
- **Consumer**: Consumes the data from the buffer.

#### **Goals of Synchronization**:
1. Ensure the producer and consumer access shared data (buffer) in a synchronized way.
2. Prevent the consumer from consuming items that have not yet been produced.
![Screenshot 2024-12-08 200605](https://github.com/user-attachments/assets/c31aac2a-a4f8-4ae7-9b1b-0ed726e77bcb)
![Screenshot 2024-12-08 200629](https://github.com/user-attachments/assets/166d5851-759b-4056-a55d-990b43a750bd)

#### **Types of Buffers**:
1. **Unbounded Buffer**:
   - No size limit.
   - The producer can always add new items, but the consumer may have to wait for new data.
2. **Bounded Buffer**:
   - Fixed size.
   - The producer must wait if the buffer is full; the consumer must wait if it’s empty.
![Screenshot 2024-12-08 200648](https://github.com/user-attachments/assets/b20dbf52-16a2-49eb-b3d7-aa83eff59bd6)

---

### **Example: Counter Variable Problem**
- The producer increments the counter (`counter++`).
- The consumer decrements the counter (`counter--`).
- Concurrent execution of these operations can lead to inconsistent results (e.g., race conditions).

#### **Race Condition**:
A scenario where:
1. Multiple processes manipulate the same shared variable concurrently.
2. The outcome depends on the order of execution.

**Example**:
- Suppose `counter = 5`.
- Two processes execute concurrently:
  - Producer executes `counter++`.
  - Consumer executes `counter--`.

Possible results: 4, 5, or 6. The only correct result is `5`.

#### **Why?**
- Both operations (`counter++` and `counter--`) involve multiple machine-level instructions.
- If these instructions interleave improperly, the counter value becomes inconsistent.

---

### **Race Condition Example with Machine Instructions**:
1. **`counter++`**:
   - Load `counter` into a register.
   - Increment the register.
   - Write back to `counter`.

2. **`counter--`**:
   - Load `counter` into a register.
   - Decrement the register.
   - Write back to `counter`.

Without synchronization:
- Producer and consumer operations may overlap, causing an incorrect final value.
![Screenshot 2024-12-08 201253](https://github.com/user-attachments/assets/44a9432e-ba88-4bfa-9d4b-8c28c5be856f)
![Screenshot 2024-12-08 201530](https://github.com/user-attachments/assets/43ac6e49-93f6-4bb1-b3f7-d641e0bca49c)
![Screenshot 2024-12-08 201922](https://github.com/user-attachments/assets/144c5380-1e40-4987-8666-ed3dfe20280a)

---

### **Solution: Process Synchronization**
We need mechanisms to prevent race conditions and ensure consistent results:
- Synchronization ensures that critical sections (where shared data is accessed) are executed by one process at a time.

---

### **Summary**
- **Process Synchronization** is essential for consistent data in systems with cooperating processes.
- **Producer-Consumer Problem** demonstrates the importance of shared memory synchronization.
- **Race Conditions** occur due to unsynchronized access to shared data.
- Proper synchronization (using locks, semaphores, or monitors) resolves these issues.
---
