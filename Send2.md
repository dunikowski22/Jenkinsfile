# Example usage
if __name__ == "__main__":
    key = "thisisaverysecretkey!"  # Must be 16, 24, or 32 bytes long
    aes = AESCipher(key)
    
    messages = [
        "Hello, Crypto! This is a secure encryption test.",
        "Another message to encrypt and decrypt.",
        "AES encryption is useful for securing data."
    ]
    
    for message in messages:
        encrypted_message = aes.encrypt(message)
        decrypted_message = aes.decrypt(encrypted_message)
        
        print("\n============================")
        print(f"Original: {message}")
        print(f"Encrypted: {encrypted_message}")
        print(f"Decrypted: {decrypted_message}")
        print("============================\n")
