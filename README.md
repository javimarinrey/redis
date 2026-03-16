# Redis

## Ver el estado de la replicación
```
redis-cli INFO replication
```

Lo que verás en el Maestro:

* **role:master:** Confirma que el nodo es el principal.

* **connected_slaves:** Número de esclavos conectados.

* **slave0, slave1...:** IP, puerto y estado de cada esclavo.

Lo que verás en el Esclavo:

* **role:slave:** Confirma que es un nodo secundario.

* **master_host:** La IP del maestro al que está apuntando.

* **master_link_status:** Debería decir up. Si dice down, hay un problema de red o de autenticación.

