Decryption

    #!/bin/bash
    
    decrypt_file() 
    {
    echo "Enter the full path of the file to decrypt (.enc file):"
    read input_file
    if [ ! -f "$input_file" ]; then
        echo "File not found!"
        return
    fi
    echo "Enter the password to decrypt the file:"
    read -s password

    output_file="${input_file%.enc}_decrypted"

    openssl enc -aes-256-cbc -d -in "$input_file" -out "$output_file" -k "$password"

    if [ $? -eq 0 ]; then
        echo "File decrypted successfully as: $output_file"
    else
        echo "Decryption failed. Wrong password or corrupt file."
    fi
    }
    while true; do
    echo ""
    echo "=============================="
    echo " Secure File Encryption System"
    echo "=============================="
    echo "1. Encrypt a File"
    echo "2. Decrypt a File"
    echo "3. Exit"
    echo "Choose an option (1-3):"
    read choice

    case $choice in
        1) encrypt_file ;;
        2) decrypt_file ;;
        3) echo "Exiting..."; break ;;
        *) echo "Invalid choice. Please try again." ;;
        esac
    done
