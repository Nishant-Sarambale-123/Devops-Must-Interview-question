### **Types of Bugs in Software (with Focus on Memory Leak Bugs)**

A **bug** is an error or flaw in a program that causes incorrect or unexpected behavior. Bugs can be classified based on **what they affect** and **when they appear**.

***

## **Common Types of Bugs**

### **1. Syntax Bugs**

*   Errors in code structure or grammar
*   Caught by the compiler  
    ✅ Example: Missing semicolon, incorrect keyword

***

### **2. Logical Bugs**

*   Code runs, but produces **wrong results**
*   Hard to detect; need testing  
    ✅ Example: Using `>` instead of `<` in a condition

***

### **3. Runtime Bugs**

*   Occur while the program is running
*   Often cause crashes or exceptions  
    ✅ Example: Null Pointer Exception, Divide by zero

***

### **4. Functional Bugs**

*   Application does not behave as per requirements  
    ✅ Example: Submit button does nothing

***

### **5. Performance Bugs**

*   Application is slow or inefficient  
    ✅ Example: Long response time, high CPU usage

***

### **6. Security Bugs**

*   Vulnerabilities that can be exploited  
    ✅ Example: SQL Injection, insecure authentication

***

### **7. UI / Visual Bugs**

*   Related to layout or appearance  
    ✅ Example: Misaligned buttons, text overlap

***

### **8. Concurrency Bugs**

*   Occur in multi‑threaded applications  
    ✅ Example: Race condition, deadlock

***

## ✅ **Which Bug Causes Memory Leak?**

### **Memory Leak is caused by:**

## **Resource Management Bugs** (a type of Runtime / Performance bug)

***

### **What is a Memory Leak?**

A **memory leak** happens when a program **allocates memory but fails to release it**, even after it’s no longer needed.

Over time, this causes:

*   Increased memory usage
*   Application slowdown
*   Application crash (OutOfMemory error)

***

### **Examples of Memory Leak Bugs**

#### **1. Unreleased Objects**

*   Objects referenced but never used again  
    ✅ Common in Java due to unused collections

#### **2. Not Closing Resources**

*   Files, DB connections, streams not closed  
    ✅ Example:

```java
FileInputStream fis = new FileInputStream(file);
// fis.close() missing
```

#### **3. Static References**

*   Static variables holding objects forever

#### **4. Event Listeners Not Deregistered**

*   Especially in UI or web apps

#### **5. Infinite Object Creation**

*   Objects created inside loops without cleanup

***

### **Bug Category for Memory Leak**

✅ **Runtime Bug**  
✅ **Performance Bug**  
✅ **Resource Management Bug** ← *Primary cause*

***

## **Simple Interview Answer**

> Memory leaks are caused by resource management bugs where the application allocates memory but fails to release it, leading to increased memory usage and potential application crashes.

***

## **One‑Line Answer (Very Short)**

> A memory leak is caused by a resource management bug where memory is not freed after use.

***

If you want, I can also explain:

*   Memory leak examples in **Java**
*   How to **detect memory leaks**
*   Tools used (Heap dump, GC logs)
*   Interview Q\&A on memory leaks

Just tell me 😊
