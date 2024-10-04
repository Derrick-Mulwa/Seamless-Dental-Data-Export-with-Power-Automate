
# **Seamless Dental Data Export using Power Automate**

## **1. Project Overview**

**Description:**  
This project focuses on developing an automated solution using **Power Automate** to streamline the process of extracting patient data from the Aligntech web platform and exporting it to OrthoCAD, a desktop application. The automation involves navigating through web pages, logging into an account, filtering and extracting relevant data, and configuring export settings in OrthoCAD through automated actions and keystrokes.

**Objectives:**
- **Main Objective:** To reduce time and manual effort in exporting patient data from the Aligntech online platform to the OrthoCAD desktop program.
- To ensure accurate and consistent data handling for patient records.
- To save exported data in a structured format within designated folders.

## **2. Project Components**

### **2.1 Tools and Technologies**
- **Power Automate:** For creating and running automation scripts that facilitate seamless interaction between web and desktop applications.
- **Google Chrome:** As the web browser for data extraction and interaction.
- **OrthoCAD:** Desktop software used for managing dental data and exporting patient files.


<br><br>**NOTE:** The data shown to you in this video is dummy and does not represent any real patient.<br><br>
### **2.2 Workflow Steps**
[Checkout the workflow video here](images/video.mp4)


1. **Launch Chrome Browser:**
   - Open a new Chrome instance and navigate to the designated URL.

2. **User Authentication:**
   - Input user credentials (username and password) to log in to the web platform.

3. **Data Navigation:**
   - Navigate to the "Orders" and "Orders List" sections to access patient data.

4. **Data Filtering:**
   - Apply filters to display only the relevant data for the current day.

5. **Data Extraction:**
   - Extract relevant patient data from the webpage and store it in a virtual table named `todaysdata`.

6. **Iterative Processing:**
   - For each item in `todaysdata`:
     - Launch a new Chrome instance.
     - Navigate to the specific URL associated with the current item.
     - Extract additional data and store it in a list named `names`.

7. **Exporting Data to OrthoCAD:**
   - Click on the "Export (OrthoCAD 3.5 or higher)" link.
   - Automate the selection of export settings using the `Send keys` function to configure:
     - **Export Type:** Selected the option "Open shell" from the dropdown list.
     - **Data Format:** Selected the option "File per arch (each arch with teeth up)" from the dropdown list.
     - **File Size:** Selected the option "High quality (large size)" from the dropdown list.
     - **Folder Name:** Inputted as "First letter of first name - Last name" in the textbox.

8. **Completion:**
   - Close all browser instances after the export process is completed.

## **3. Output and Data Management**
- The exported patient data is saved in a designated folder named according to the specified format (first letter of the first name - last name). This folder contains essential files, including the patient's dental photos and `.stl` files.

## **4. Benefits of the Automation**
- **Increased Efficiency:** The automation significantly reduces the time and effort required for data extraction and export processes.
- **Error Reduction:** Minimizes the likelihood of human error during data handling.
- **Structured Data Organization:** Saves exported files in a clear and organized manner, facilitating easy access and retrieval.


## **6. Conclusion**
The **Automated Dental Data Transfer to OrthoCAD** project, powered by **Power Automate**, successfully automates a critical workflow in managing dental patient data, integrating browser automation with desktop application functionality. This solution enhances efficiency, accuracy, and organization of patient records, providing a valuable tool for dental professionals.
