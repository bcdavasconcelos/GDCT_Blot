tags: Time-machine

# Backup

## Time-machine
O primeiro backup com o time-machine pode levar muito tempo. Para remover as restrições de uso do CPU para a realização do backup, use o comando:

```bash
sudo sysctl debug.lowpri_throttle_enabled=0
```

Para restaurar a proteção contra o uso excessivo do CPU pelo time-machine, use o comando:

```bash
Sudo sysctl debug.lowpri\_throttle_enabled=1
```

#MacOS/Timemachine