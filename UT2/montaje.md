# SI · UT2 — Ficha de taller: montaje y revisión de un ordenador


# UT2 · Práctica de montaje de equipo

**Autores:** David Membrives Muñoz · Javier Pulido Calvo
**Equipo:** A
**Módulo:** Sistemas Informáticos · Curso 2026/27
**Centro:** IES Politécnico Hermenegildo Lanz
**Fecha de la práctica:** 16 de noviembre de 2026

---

## 1. Tabla de componentes del equipo montado

| Componente | Marca / modelo | Características identificadas | Foto |
|---|---|---|---|
| Chasis | Negro, sobremesa de formato reducido (marca no identificada) | Ventilación lateral, panel frontal con USB y botón de encendido | [01](img/01-exterior-caja.jpg) |
| Placa base | Gigabyte GA-B85M-DS3H (rev. 3.0) | Micro-ATX, socket LGA1150, chipset Intel B85, 4 ranuras DDR3, ranura PCIe x16, 2 ranuras PCIe x1, SATA 6 Gb/s, salidas VGA/DVI/HDMI, UEFI DualBIOS | [04](img/04-placa-base-gigabyte.jpg) |
| Procesador (CPU) | Intel Celeron G1840 (SR1VK) | 2,80 GHz, socket LGA1150, fabricado en Costa Rica | [10](img/10-cpu-celeron-g1840.jpg) |
| Disipador y ventilador | Intel de serie, Foxconn CNFN4344V2 | 12 V, 0,17 A, conector de 4 pines conectado en `CPU_FAN` | [11](img/11-disipador-intel.jpg) |
| Memoria RAM | Crucial CT25664BA160B | 2 GB, DDR3, DIMM de 240 pines | [08](img/08-ram-crucial.jpg) |
| Almacenamiento | WD Blue WD5000AAKX | 500 GB, SATA, 16 MB de caché, formato 3,5" | [02](img/02-interior-almacenamiento.jpg) |
| Fuente de alimentación | Power Man IP-S300EF7-2 H | 300 W, formato TFX, con sello 80 PLUS | [06](img/06-fuente-alimentacion.jpg) |
| Tarjeta de expansión | Tarjeta WiFi PCIe x1 (marca no visible) | 300 Mbps, 2,4 GHz, IEEE 802.11 b/g/n, 2 antenas SMA, soporte de perfil bajo | [12](img/12-tarjeta-wifi.jpg) |
| Conexiones frontales | Cableado del chasis | USB frontales en `F_USB1` y `F_USB2`, panel frontal en `F_PANEL` (HDD LED, power, reset) | [15](img/15-f-usb-y-f-panel.jpg) |

---

## 2. Fotos de las fases importantes

Las fotos están en `UT2/img/`.

### 2.1 Estado inicial y apertura

Aspecto exterior del equipo antes de abrirlo, con arañazos y marcas de uso en el lateral.

![Exterior de la caja](img/01-exterior-caja.jpg)

Interior abierto, con la jaula de unidades sacada y el disco duro a la vista.

![Apertura e interior](img/03-apertura-interior.jpg)

### 2.2 Placa base

Placa base Gigabyte GA-B85M-DS3H con el disipador montado, fuera del chasis.

![Placa base](img/04-placa-base-gigabyte.jpg)

Placa base atornillada en el chasis.

![Placa montada](img/05-placa-montada-chasis.jpg)

### 2.3 Fuente de alimentación

Fuente Power Man de 300 W con todo su cableado: conector de 24 pines, conector de 4+4 pines para la CPU y conectores SATA.

![Fuente de alimentación](img/06-fuente-alimentacion.jpg)

Fuente colocada en su alojamiento.

![Fuente montada](img/07-fuente-montada.jpg)

### 2.4 Memoria RAM

Módulo Crucial de 2 GB DDR3 extraído, junto con los dos tornillos que sujetaban la tarjeta de expansión.

![Memoria RAM](img/08-ram-crucial.jpg)

### 2.5 Almacenamiento

Disco duro WD Blue de 500 GB en su jaula, con las guías amarillas de sujeción sin herramientas.

![Almacenamiento](img/02-interior-almacenamiento.jpg)

### 2.6 CPU y disipador

Socket LGA1150 con la palanca levantada y la CPU colocada. Se aprecia restos de pasta térmica sobre el procesador.

![Socket con CPU](img/09-socket-cpu.jpg)

Detalle del procesador Intel Celeron G1840 a 2,80 GHz.

![CPU Celeron G1840](img/10-cpu-celeron-g1840.jpg)

Disipador de serie de Intel con su ventilador de 4 pines.

![Disipador Intel](img/11-disipador-intel.jpg)

### 2.6 bis Conexión del ventilador de la CPU

El conector de 4 pines del ventilador va en `CPU_FAN`.

![Conector CPU_FAN](img/14-conector-cpu-fan.jpg)

### 2.7 Tarjeta de expansión (WiFi PCIe x1)

![Tarjeta WiFi](img/12-tarjeta-wifi.jpg)

![Tarjeta WiFi con soporte](img/13-tarjeta-wifi-bracket.jpg)

### 2.8 Reconexión y orden de cables

Cabezales `F_USB1` y `F_USB2` con los cables USB frontales y panel frontal `F_PANEL`.

![F_USB y F_PANEL](img/15-f-usb-y-f-panel.jpg)

![Cabezales USB](img/16-cabezales-usb.jpg)

Cables del panel frontal (HDD LED, power y reset) conectados en `F_PANEL`.

![Cables del panel frontal](img/17-cables-panel-frontal.jpg)

### 2.9 Ficha de taller

Ficha de taller (página 3/6) con el registro del trabajo, la incidencia y la comprobación final. Se incluye como referencia de lo realizado.

![Ficha de taller, página 3/6](img/18-ficha-taller-pag3.jpg)

---

## 3. Primer arranque y ajustes de la UEFI

El equipo **no se encendió** durante la práctica, porque no se autorizó el encendido (en la ficha, «¿Encendido autorizado?» queda sin marcar). Por tanto, no hay primer arranque ni ajustes de UEFI que documentar.

Como referencia, la placa Gigabyte GA-B85M-DS3H incorpora UEFI DualBIOS (ver [foto de la placa](img/04-placa-base-gigabyte.jpg)).

---

## 4. Salida comentada de `lscpu`, `free -h`, `lsblk`, `lspci` y `lsusb`

El equipo montado no se arrancó, así que los comandos se ejecutaron en otro equipo: un portátil **HP Laptop 15-db0074ns** (ProdID 6EK93EA#ABE) con Windows, usando **Ubuntu sobre WSL2**. Por eso los datos corresponden al portátil y no al equipo del taller (Celeron G1840).

![Etiqueta del portátil HP](img/19-portatil-hp-etiqueta.jpg)

### `lscpu`

![Salida de lscpu](img/22-lscpu.png)

- **Arquitectura:** `x86_64`, con modos de 32 y 64 bits.
- **Procesador:** `AMD A6-9225 RADEON R4, 5 COMPUTE CORES 2C+3G`, es decir, 2 núcleos de CPU y 3 de gráficos integrados (familia 21, modelo 112).
- **Núcleos e hilos:** 1 socket, 2 núcleos y 1 hilo por núcleo, así que `CPU(s): 2`.
- **Cachés:** L1d de 64 KiB, L1i de 192 KiB y L2 de 2 MiB.
- **Virtualización:** el hipervisor es Microsoft y el tipo es `full`, lo que confirma que Linux corre dentro de WSL2 y no directamente sobre el hardware.
- **Flags:** incluyen `aes`, `avx`, `avx2` y `sse4_2`, entre otras extensiones.
- **Vulnerabilidades:** las visibles en la captura aparecen como `Not affected`.

### `free -h`

![Salida de free -h](img/23-free-h.png)

- **Memoria total:** 3,6 GiB, de los que hay 407 MiB usados, 3,1 GiB libres y 3,2 GiB disponibles. El resto de la RAM física la gestiona Windows.
- **Caché:** 139 MiB en `buff/cache`.
- **Swap:** 1,0 GiB, sin usar.

### `lsblk`

![Salida de lsblk](img/24-lsblk.png)

- **`sda`:** 722,9 MiB, de solo lectura (`RO 1`).
- **`sdb`:** 97,4 MiB, de solo lectura, montado en `/usr/src/linux-headers-6.18.58.1-microsoft-standard-WSL2`.
- **`sdc`:** 1 GiB, usado como `[SWAP]`.
- **`sdd`:** 1 TiB, montado en `/` y en `/mnt/wslg/distro`. Es el disco virtual que contiene todo el sistema de Ubuntu.

Son discos virtuales de WSL2, no los discos físicos del portátil.

### `lspci` y `lsusb`

Primero hubo que instalar los paquetes con `sudo apt install pciutils usbutils`, porque los comandos no existían (`command not found`).

![Salida de lspci y lsusb](img/25-lspci-lsusb.png)

- **`lspci`** muestra solo tres dispositivos, todos virtuales:
  - un controlador 3D, `Microsoft Corporation Basic Render Driver`, que es la GPU virtual que WSL2 ofrece a Linux;
  - un controlador de almacenamiento SCSI `Red Hat, Inc. Virtio 1.0 console`;
  - un periférico de sistema `Red Hat, Inc. Virtio 1.0 file system`, que sirve para compartir archivos con Windows.
- **`lsusb`** no muestra ningún dispositivo, porque WSL2 no expone los puertos USB del portátil a Linux por defecto.

En ninguno de los dos aparece el hardware físico real del portátil (la gráfica AMD Radeon R4, la tarjeta de red, etc.), solo el hardware virtual que crea WSL2. En una instalación de Linux sobre el equipo, o con un Linux en modo live, saldría el hardware real.

---

## 5. Uso de IA

Durante la práctica de montaje se consultó a una IA en dos ocasiones, para resolver dudas puntuales de conexión:

1. **¿Dónde se conecta el cable SATA?** Se envió una foto del interior del equipo.

   ![Consulta sobre el cable SATA](img/20-ia-consulta-sata.png)

2. **¿Dónde se conecta el cable `SPEAKER` en la placa Gigabyte GA-B85M-DS3H?** Consulta realizada el lunes 16 de noviembre a las 12:59.

   ![Consulta sobre el conector SPEAKER](img/21-ia-consulta-speaker.png)

La IA solo sirvió de apoyo para esas dos dudas. El desmontaje, el montaje, las fotos y el registro en la ficha los hicimos nosotros.

Este documento se ha redactado con ayuda de Claude (Anthropic) a partir de nuestras fotos y de la información que le facilitamos. Los datos de la tabla salen de las etiquetas visibles en las fotos.
