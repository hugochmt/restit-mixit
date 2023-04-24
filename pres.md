---
marp: true
backgroundColor: #2c233d
color: white
style: |
  section {
    justify-content: start;
  }

  secction.imgList img {
    display: block;
  }
---

# Restitution MiXiT 2023 🥞

![bg w:650](./imgs/mxt-icon--logo.svg)


---

![bg w:900](./imgs/photo.jpg)

---
# Cache Http

...

---
# Systèmes distribués

## Saga pattern

---
<!-- _class: imgList -->
# Systèmes distribués

## Outbox pattern
- Garantir l'intégrité des transactions dans les architectures basées sur des évènements :
- Stockage des évènement dans une table en base de données
- Un processus asynchrone récupère les évènements non-publiés et s'occupe de les publier dans le broker

![bg left:40% w:90%](./imgs/outbox1.png)

---
# Systèmes distribués

- Timeout courts
  - Pourquoi faire attendre le client trop longtemps si un service est potentiellement tombé ?

- Exponential backoff
  - Attendre de plus en plus longtemps entre des requêtes tombant en échec

- Circuit breaker pattern

---
# WebAssembly

![bg w:80%](./imgs/wasm_schema.jpg)

---

## Promesses

- Compilation de différents langages vers un même binaire `wasm`
- Runtimes WebAssembly :
  - Navigateur
  - Node.js
- Vitesse d'exécution améliorée
- Portabilité
- Sécurité (éxecution dans un contexte sandbox)

---
# WebAssembly
## Etat actuel
- V 2.0 (2019)
- Langages supportés (Browser) :
  - C/C++
  - Rust
  - Java
  - Python ⏳
- Langages spécifiques :
  - Grain
  - AssemblyScript (TypeScript-like)

---
# WebAssembly

## Etat actuel

- Docker + WASM (beta)

- WebAssembly System Interface (WASI) :
  - System interface to run WebAssembly outside the web
- Component model
