# password-cracking-tool
import hashlib

def hash_password(password, algorithm='sha256'):
    if algorithm == 'md5':
        return hashlib.md5(password.encode()).hexdigest()
    elif algorithm == 'sha1':
        return hashlib.sha1(password.encode()).hexdigest()
    elif algorithm == 'sha256':
        return hashlib.sha256(password.encode()).hexdigest()
    else:
        raise ValueError("Unknown algorithm")

password = 'password123'
hashed_password = hash_password(password, 'sha256')
print(f'Hashed password: {hashed_password}')

cyber securtiy project using python
