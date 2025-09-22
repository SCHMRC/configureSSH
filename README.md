# Configurare SSH per utilizzo di GitHub da CLI

Per utilizzare GitHub da riga di comando windows è necessario inizialmente creare una chiave che utilizzi l'algoritmoo di crittografia asimmetrico RSA e generare quindi lo coppia di chiavi pubblica/privata che permetta di effettuare il collegamento sicuro tra i dispositivi.

Di seguito viene riportata la procedura per effettuare la creazione della coppia di chiavi:

- crea la coppia di chiavi:
    ```
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ```
    sostituisci  your_email@example.com con la mail di accesso a github;
    Puoi anche utilizzare RSA:
    ```
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```
- Quando ti viene chiesto dove salvare la chiave premi enter per confermare il percorso di default
- Puoi opzionalmente digirare una chiave segreta per aggiungere un ulteriore grado di sicurezza;
- <img width="1293" height="961" alt="immagine" src="https://github.com/user-attachments/assets/9c2fa63c-89ee-4d45-9a1c-cb5471f6dea0" />
- aggiungere la chiave SSH al tuo account GITHUB, copia il contenuto dei file
    ```
    cat ~/.ssh/id_ed25519.pub
    ```
    se hai generato una chiave RSA:
    ```
    cat ~/.ssh/id_rsa.pub
    ```
- apri il tuo account GITHUB es accedi alla sezione SSH e GPG keys
- <img width="1414" height="1221" alt="immagine" src="https://github.com/user-attachments/assets/7d2048f1-5c3e-4841-b2f9-48c4dc29f0be" />

- clicca su New SSH key
- <img width="1597" height="1317" alt="immagine" src="https://github.com/user-attachments/assets/6a5cf0a0-377f-4cee-85ea-7721cbd261fa" />

- compila  campi e incolla la chiave generata in locale all'interno della sezione key
- in fine clicca su add SSH KEY
- <img width="1500" height="1146" alt="immagine" src="https://github.com/user-attachments/assets/e235bf5d-0f61-48e0-8ff4-33ce71352d8e" />

---
## Sitografia:
<a href="https://www.geeksforgeeks.org/git/how-to-add-ssh-key-to-your-github-account/">geeksforgeeks</a>


