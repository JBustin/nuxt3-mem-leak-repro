# Reproduction

```sh
git clone https://github.com/JBustin/nuxt3-mem-leak-repro.git
```
```sh
npm ci
```
```sh
NUXT_PUBLIC_API_KEY=MYKEYVALUE npm run inspect
```

Open the Chrome inspector, at this address: `chrome://inspect/#devices`.

Run the load test in a new terminal (~600 requests during 30s):
```sh
npm run load-test
```

Make a heap snapshot.

Search for `MYKEYVALUE` in the generated heap snapshot.

You should see the same number of records in memory than the number of requests generated by the load tests (~600).

<img width="1449" alt="Capture d’écran 2024-12-19 à 16 08 39" src="https://github.com/user-attachments/assets/6d14bfe9-3e1b-4f92-8ec9-4d15904977d0" />

