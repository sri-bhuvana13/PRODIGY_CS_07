def encrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            
            shift_base = ord('A') if char.isupper() else ord('a')
      
            result += chr((ord(char) - shift_base + shift) % 26 + shift_base)
        else:
…shift_value = 3

encrypted_text = encrypt(text, shift_value)
print(f"Encrypted Message: {encrypted_text}")

decrypted_text = decrypt(encrypted_text, shift_value)
print(f"Decrypted Message: {decrypted_text}")
