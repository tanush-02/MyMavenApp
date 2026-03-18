# 🚀 Maven Project Setup & Dependency Management

This project demonstrates how to create a Maven-based Java application, understand the POM file, add dependencies, and build/run the project.

---

## 📌 Program 1: Working with Maven

### 🛠️ Step 1: Create a Maven Project

Run the following command in terminal:

```bash
mvn archetype:generate \
-DgroupId=com.example \
-DartifactId=MyMavenApp \
-DarchetypeArtifactId=maven-archetype-quickstart \
-DinteractiveMode=false
```

This generates:
- App.java (Main class)
- AppTest.java (Test class)

BUILD SUCCESS confirms project creation.

---

### 📁 Step 2: Navigate to Project

```bash
cd MyMavenApp
```

---

### 📄 Step 3: Edit pom.xml

Open file:

```bash
gedit pom.xml
```

#### ➤ Add JUnit Dependency

Go to https://mvnrepository.com → Search "JUnit" → Copy latest dependency

Paste inside `<dependencies>`:

```xml
<dependencies>
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.13.2</version>
        <scope>test</scope>
    </dependency>
</dependencies>
```

---

### ✏️ Step 4: Update App.java

```java
public class App {
    public static void main(String[] args) {
        System.out.println("Hello, Maven Project!");
    }
}
```

---

### ⚙️ Step 5: Compile Project

```bash
mvn compile
```

BUILD SUCCESS means successful compilation.

---

### 📦 Step 6: Package Project

```bash
mvn package
```

Generates JAR file in `target/`

---

### 🧪 Step 7: Run Tests

```bash
mvn test
```

---

### ▶️ Step 8: Run Application

```bash
cd target
java -jar MyMavenApp-1.0-SNAPSHOT.jar
```

Output will match App.java code.

---

## 📦 Dependency Management

Maven uses `pom.xml` to manage:
- Dependencies
- Plugins
- Build lifecycle

---

## 🔧 Additional Libraries

### 🔹 Google Guava

Features:
- Advanced Collections (Multimap, ImmutableList)
- Functional utilities
- Caching
- String utilities
- Concurrency tools

```xml
<dependency>
  <groupId>com.google.guava</groupId>
  <artifactId>guava</artifactId>
  <version>32.1.2-jre</version>
</dependency>
```

---

### 🔹 Apache Commons IO

Features:
- File operations (FileUtils)
- Stream utilities (IOUtils)
- Directory monitoring
- File filtering

```xml
<dependency>
  <groupId>commons-io</groupId>
  <artifactId>commons-io</artifactId>
  <version>2.15.1</version>
</dependency>
```

---

## 📂 Project Structure

```bash
MyMavenApp/
│── src/
│   ├── main/java/com/example/App.java
│   └── test/java/com/example/AppTest.java
│── target/
│── pom.xml
```

---

## ✅ Conclusion

This project covers:
- Maven project creation
- Understanding POM.xml
- Adding dependencies (JUnit, Guava, Commons IO)
- Build, test, and execution workflow

---

## 📚 References

- https://maven.apache.org/
- https://mvnrepository.com/

---

## 👨‍💻 Author

Dept. of CSE, BIT  
Academic Year: 2025-26
