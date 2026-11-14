# TabletGuard — Atualizações oficiais

Este repositório público contém **somente os APKs de instalação**, os checksums SHA-256 e as notas das versões do aplicativo TabletGuard.

O código-fonte é mantido em um repositório privado. **Não publique** neste repositório chaves de assinatura, senhas, credenciais Firebase ou tokens.

## Como funciona no aplicativo

1. O usuário toca em **Verificar atualizações**.
2. O TabletGuard consulta `/releases/latest` pela API pública do GitHub.
3. Se existir uma versão mais recente, o usuário decide se quer **baixar**.
4. Antes de instalar, o aplicativo verifica o SHA-256, o nome do pacote e a assinatura do APK.
5. O Android apresenta a confirmação de instalação. Não existe instalação automática ou silenciosa.

## Download

As versões oficiais ficam na página de [Releases](https://github.com/projetosperalta-debug/TabletGuard-Updates/releases).

> **Ainda não há uma versão publicada.** A primeira publicação exige uma chave de assinatura permanente e a configuração do fluxo de publicação no repositório privado.

## Segurança

- Nome de pacote: `com.tabletguard.app`.
- Todas as atualizações devem ser assinadas com a **mesma chave** usada no APK instalado.
- O número `versionCode` deve aumentar a cada nova versão.
- O usuário precisa autorizar o download e a instalação.
- Se uma versão anterior foi assinada com outra chave (por exemplo, debug temporário), o Android não permitirá instalá-la por cima. Faça backup dos dados antes de migrar para a versão assinada permanentemente.
