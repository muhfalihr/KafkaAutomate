# KafkaAutomate

### Description

This repository contains a bash script for managing Apache Kafka topics and consumer groups. The script provides an interactive command-line interface to create, describe, list, and delete topics, as well as manage consumer groups and produce/consume messages. 

### Features
- **Create Topic:** Create a new Kafka topic with optional partition configuration.
- **Describe Topic:** Retrieve details of a specific Kafka topic.
- **List Topics:** List all Kafka topics.
- **Delete Topic:** Delete a specific Kafka topic.
- **List Consumer Groups:** List all consumer groups associated with a specific topic.
- **Describe All Consumer Groups:** Get details of all consumer groups across all topics.
- **Message Producer:** Produce messages to a specified Kafka topic.
- **Message Consumer:** Consume messages from a specified Kafka topic, with an option to specify a consumer group.

### Usage

```bash
kafka_automate [option]

Options:
  --ctop       Create a new topic
  --desctop    Topic Details
  --ltop       List topics
  --dtop       Delete a topic
  --lcg        List of Consumer Group
  --descgall   Details of All Consumer Group
  --prod       Message producer
  --cons       Message consumer
  --help       Show usage information
```

### Requirements
- Apache Kafka installed and configured on your system.
- Before running the script, ensure you have `figlet` installed on your system. `figlet` is a command-line tool for creating large text banners.

    #### Installation Instructions:

    - **Ubuntu/Debian**:
        ```bash
        sudo apt-get update
        sudo apt-get install figlet
        ```

    - **Fedora**:
        ```bash
        sudo dnf install figlet
        ```

    - **Arch Linux**:
        ```bash
        sudo pacman -S figlet
        ```

    - **macOS** (using Homebrew):
        ```bash
        brew install figlet
        ```

### Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/muhfalihr/KafkaAutomate.git
    cd KafkaAutomate
    chmod +x kafka_automate
    ```
2. Setting Up Environment Variables

    To set up the necessary environment variables, follow these steps:

    1. **Open your shell configuration file**:
    - For **Zsh** (`~/.zshrc`):
        ```bash
        nano ~/.zshrc
        ```
    - For **Bash** (`~/.bashrc` or `~/.bash_profile`):
        ```bash
        nano ~/.bashrc
        ```
        or

        ```bash
        nano ~/.bash_profile
        ```

    2. **Add the environment variables to the file**:

        Append the following lines to the end of your configuration file:

        ```bash
        export HOST_NODE=<ipnode>
        export PATH=$PATH:/path/to/directory/kafka
        export KAFKA_CONFIG=/path/to/directory/kafka/config
        ```

        Replace `ipnode`, `/path/to/directory/kafka`, and `/path/to/directory/kafka/config` with your actual node IP, Kafka directory path, and Kafka configuration directory path, respectively.

        3. **Save and close the file**:
        - If you are using `nano`, press `CTRL + X`, then press `Y`, and hit `Enter`.

        4. **Apply the changes**:

        - For **Zsh**:
            ```bash
            source ~/.zshrc
            ```
        - For **Bash**:
            ```bash
            source ~/.bashrc
            ```
            or
            ```bash
            source ~/.bash_profile
            ```

        ### Example

        Here is an example with placeholder values replaced:

        ```bash
        export HOST_NODE=192.168.1.10
        export PATH=$PATH:/usr/local/kafka
        export KAFKA_CONFIG=/usr/local/kafka/config
        ```

        By following these steps, the environment variables `HOST_NODE`, `PATH`, and `KAFKA_CONFIG` will be set up and available for use in your terminal sessions.

### Running the Script
To run the script, use the following command:
```bash
kafka_automate [option]
```

For example, to create a new topic:
```bash
kafka_automate --ctop
```

<video src="https://youtu.be/euke6YCLyes?si=K2ugDkNnUVe5bwYY" width="640" height="360" controls></video>

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Contributing
Contributions are welcome! Please open an issue or submit a pull request.

### Author
[muhfalihr](https://github.com/muhfalihr)

---