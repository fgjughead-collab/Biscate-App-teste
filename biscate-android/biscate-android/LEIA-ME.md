# Biscate – APK de teste (Android 6 → mais recente)

App Android nativa (WebView) que embute o protótipo `biscate/` (site + app clicável).
Funciona offline; só o tipo de letra Inter precisa de internet (senão usa o do sistema).

- minSdk 23 (Android 6.0) · targetSdk 35 (Android 15)
- Assinada com chave debug: instala directamente, não serve para a Play Store.

## Gerar o APK (opção A – GitHub, sem instalar nada)
1. Cria um repositório no GitHub e envia o conteúdo desta pasta.
2. Separador **Actions** → "Build APK de teste" → **Run workflow**.
3. Quando terminar (~3-5 min), descarrega o artefacto **Biscate-teste-apk** (contém `app-debug.apk`).

## Gerar o APK (opção B – Android Studio)
1. Abre esta pasta no Android Studio → espera o Gradle sincronizar.
2. **Build → Build APK(s)**. Ficheiro em `app/build/outputs/apk/debug/app-debug.apk`.

## Instalar no telemóvel
Envia o `.apk` para o telemóvel, abre-o e permite "Instalar apps de fontes desconhecidas" quando pedir.

## Nota
Isto empacota o protótipo estático. A app full-stack (React + backend Node/Postgres) precisa de um servidor online;
quando o tiveres, basta apontar `START_URL` em `MainActivity.java` para o endereço https dele.
