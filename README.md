
  <h1>Análisis de Red con Nmap</h1>

  <h2>Objetivo</h2>
  <p>
    Realizar un <strong>análisis completo de la red local</strong> utilizando <strong>Nmap</strong> para descubrir hosts activos,
    escanear puertos, identificar servicios y detectar posibles vulnerabilidades.
  </p>

  <hr>

  <h2>Comandos Ejecutados</h2>

  <h3>1. Descubrimiento de Hosts en la Red</h3>
  <pre><code>sudo nmap -sn 192.168.1.0/24</code></pre>
  <p><strong>Propósito:</strong> Identificar todos los dispositivos activos en la red local.</p>

  <h3>2. Escaneo Básico del Router</h3>
  <pre><code>sudo nmap -sS -sV 192.168.1.1</code></pre>
  <p><strong>Propósito:</strong> Analizar los puertos y servicios del router/gateway de la red.</p>

  <h3>3. Escaneo Completo Local</h3>
  <pre><code>sudo nmap -sS -sV -sC -O localhost</code></pre>
  <p><strong>Propósito:</strong> Realizar un escaneo exhaustivo de la máquina local incluyendo detección de sistema operativo y ejecución de scripts básicos.</p>

  <h3>4. Análisis de Seguridad</h3>
  <pre><code>sudo nmap --script safe 192.168.1.1</code></pre>
  <p><strong>Propósito:</strong> Ejecutar scripts de seguridad para identificar configuraciones inseguras.</p>

  <hr>

  <h2>Información Obtenida</h2>

  <h3>Descubrimiento de Hosts</h3>
  <ul>
    <li>Lista completa de dispositivos activos en la red.</li>
    <li>Direcciones IP y MAC de cada host.</li>
    <li>Fabricantes de tarjetas de red.</li>
    <li>Tiempos de respuesta de los dispositivos.</li>
  </ul>

  <h3>Escaneo de Puertos y Servicios</h3>
  <ul>
    <li>Puertos abiertos en cada dispositivo.</li>
    <li>Servicios ejecutándose en cada puerto.</li>
    <li>Versiones específicas de software.</li>
    <li>Banners e información de servicios.</li>
  </ul>

  <h3>Análisis de Seguridad</h3>
  <ul>
    <li>Configuraciones inseguras en servicios.</li>
    <li>Servicios desactualizados.</li>
    <li>Puertos sensibles expuestos.</li>
    <li>Recomendaciones de hardening.</li>
  </ul>

  <h3>Detección de Sistemas Operativos</h3>
  <ul>
    <li>Tipo y versión de sistema operativo en hosts.</li>
    <li>Arquitectura de hardware.</li>
    <li>Información específica del kernel.</li>
  </ul>

  <hr>

  <h2>Técnicas Utilizadas</h2>

  <h3>Escaneo SYN (-sS)</h3>
  <ul>
    <li>Escaneo half-open más rápido y sigiloso.</li>
    <li>Evita completar el handshake TCP.</li>
    <li>Ideal para evadir detección básica.</li>
  </ul>

  <h3>Detección de Versiones (-sV)</h3>
  <ul>
    <li>Analiza respuestas de los servicios.</li>
    <li>Compara con base de datos de firmas.</li>
    <li>Identificación precisa de software.</li>
  </ul>

  <h3>Scripting Engine (-sC)</h3>
  <ul>
    <li>Ejecución de scripts NSE básicos.</li>
    <li>Automatiza pruebas comunes.</li>
    <li>Recolecta información adicional.</li>
  </ul>

  <h3>Detección de Sistema Operativo (-O)</h3>
  <ul>
    <li>Analiza el stack TCP/IP.</li>
    <li>Detecta patrones de respuesta específicos.</li>
    <li>Identifica el sistema operativo del host.</li>
  </ul>

  <hr>

  <h2>Resultados del Análisis</h2>
  <p>El análisis proporcionó una visión completa de:</p>
  <ul>
    <li>Topología de la red local.</li>
    <li>Dispositivos conectados y sus roles.</li>
    <li>Servicios expuestos y su estado de seguridad.</li>
    <li>Puntos potenciales de entrada para atacantes.</li>
    <li>Recomendaciones para mejorar la seguridad.</li>
  </ul>

  <hr>

  <h2>Aplicaciones Prácticas</h2>
  <ul>
    <li>Auditorías de seguridad periódicas.</li>
    <li>Hardening de sistemas y servicios.</li>
    <li>Detección de dispositivos no autorizados.</li>
    <li>Planificación de estrategias de seguridad.</li>
    <li>Cumplimiento de políticas de seguridad informática.</li>
  </ul>

</body>
</html>
