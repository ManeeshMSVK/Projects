Encryption

    #!/bin/bash
     
     encrypt_file()
     {
    echo "Enter the full path of the file to encrypt:"
    read input_file
    if [ ! -f "$input_file" ]; then
        echo "File not found!"
        return
    fi
    echo "Enter a password to encrypt the file:"
    read -s password
    output_file="${input_file}.enc"
    openssl enc -aes-256-cbc -salt -in "$input_file" -out "$output_file" -k "$password"
    if [ $? -eq 0 ]; then
        echo "File encrypted successfully as: $output_file"
    else
        echo "Encryption failed."
    fi
    }
