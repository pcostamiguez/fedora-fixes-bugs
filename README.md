# fedora-fixes-bugs

## Fedora KDE Black Screen on startup fix:

- EN:
There is a known issue with lots of hardware that the kde desktop does not load and you just sit on a black screen after install. If this happens to you, you will need to reboot, on the grub page, hit "e" and add the word "nomodeset" after the word "quiet". Once you do that it will boot in the fallback desktop. *Don't try to install any drivers*. Just run the system upgrade and it will resolve the missing dependencies for your hardware. Then let it reboot. This will fix the blank screen issue, and boot correctly to your login page and functioning kde desktop. From there you can install your GPU drivers. For nvidia it would be "sudo dnf install nvidia-drivers" Then you can run nvidia-smi to verify that the driver installed.

- PT-BR:
Existe um problema conhecido com diversos hardwares em que o desktop KDE não carrega e o sistema fica apenas em uma tela preta após a instalação. Se isso acontecer com você, será necessário reiniciar o computador e, na tela do GRUB, pressionar “e” e adicionar a palavra “nomodeset” após a palavra “quiet”.
Ao fazer isso, o sistema irá iniciar usando o desktop de contingência (fallback). Não tente instalar nenhum driver nesse momento. Apenas execute a atualização do sistema, pois ela irá resolver as dependências ausentes para o seu hardware. Em seguida, permita que o sistema reinicie.
Isso corrigirá o problema da tela preta e o sistema iniciará corretamente, exibindo a tela de login e um desktop KDE funcional. A partir daí, você poderá instalar os drivers da sua GPU.
No caso de placas NVIDIA, o comando é:
sudo dnf install nvidia-drivers

Depois disso, você pode executar nvidia-smi para verificar se o driver foi instalado corretamente.
