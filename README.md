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

