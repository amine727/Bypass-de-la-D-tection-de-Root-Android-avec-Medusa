# 🔐 LAB 12 – Bypass Root Detection Android avec Medusa

---

## 🎯 Objectif

Réaliser un bypass de la détection de root sur une application Android (DIVA) en utilisant **Frida** et **Medusa**.

---

## 🧰 Outils utilisés

* Frida
* Medusa
* ADB (Android Debug Bridge)
* Android Emulator
* Application DIVA

---

## ⚙️ Étapes réalisées

---

## 1️⃣ Installation de Medusa

<img width="1473" height="679" alt="5" src="https://github.com/user-attachments/assets/0c15eb84-51d6-4b75-9780-c1a28b5d206e" />

Clonage du projet et installation des dépendances :

```bash id="r3q5s7"
git clone https://github.com/Ch0pin/medusa.git
cd medusa
pip install -r requirements.txt
```

---

## 2️⃣ Lancement de Medusa

<img width="990" height="578" alt="6" src="https://github.com/user-attachments/assets/7d89b775-d63a-4f7b-a120-fdfcca18608b" />

Exécution de Medusa et détection de l’appareil Android :

```bash id="0o5f0n"
python medusa.py -p jakhar.aseem.diva
```

---

## 3️⃣ Identification du processus cible

<img width="1025" height="713" alt="7" src="https://github.com/user-attachments/assets/af43b879-0d79-4d9f-bcce-455af6256b72" />

Récupération du PID de l’application avec Frida :

```bash id="g0u3hs"
frida-ps -Uai
```

Exemple :

```text id="rg9v07"
10464  Diva   jakhar.aseem.diva
```

---

## 4️⃣ Injection du module de bypass

<img width="1055" height="549" alt="8" src="https://github.com/user-attachments/assets/9b35e237-8ac5-49b0-9679-d5bc25bfcf68" />

Chargement et exécution du module de bypass :

```bash id="0rt7fd"
use root_detection/universal_root_detection_bypass
run -p 10464
```

---

## ✅ Résultat

* Connexion Frida établie ✔
* Script injecté avec succès ✔
* Hooks actifs ✔
* Détection de root contournée ✔

---



## 🔐 Conclusion

Ce lab démontre que les mécanismes de sécurité côté client peuvent être contournés à l’aide d’outils comme Medusa et Frida.

---

