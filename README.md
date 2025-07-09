# ProyectoFinaldeCiberseguridad_4Geeks
Proyecto Final de Ciberseguridad 4Geeks Academy
Informe Forense y Pentesting — Caso de Incidente en Servidor Debian en 4Geeks
Alumno: Simón A. Cervantes Martínez
Fecha última revisión: 14/07/2025

Índice
1.Introducción
•Objetivo general del proyecto
•Contexto (simulación de empresa 4Geeks)
•Alcance del análisis
•Enfoque profesional asumido (SOC, Blue Team, análisis forense, etc.)
•Herramientas utilizadas (Kali Linux, Nmap, Autopsy, chkrootkit, etc.)

2.Metodología de análisis
•Enfoque técnico seguido (pasos NIST / ISO / ciclo forense)
•Fases: Reconocimiento, análisis, mitigación, hardening
•Consideraciones éticas y forenses (no alterar pruebas, documentación constante)

3.Fase 1: Corrección del hackeo
3.1 Identificación del incidente
•Servicios comprometidos
•Vía de entrada (logins sospechosos, logs revisados)
•Línea de tiempo del ataque
3.2 Recolección de evidencia
•Logs clave analizados (auth.log, syslog)
•Procesos sospechosos
•Cuentas de usuario maliciosas
•Archivos modificados
•Comandos clave usados
3.3 Escaneo y eliminación de malware
•Herramientas: chkrootkit, rkhunter, debsums, etc.
•Resultados del escaneo
3.4 Mitigación del ataque
•Exploit bloqueado
•Usuarios eliminados
•Backdoors desactivados
•Servicios detenidos temporalmente
3.5 Fortalecimiento inmediato
•Actualización de paquetes
•Cambio de contraseñas
•Configuración de firewall y SSH
3.6 Evidencia de mitigación
•Capturas o logs de configuración corregida
•Servicios reiniciados y validados

4.Fase 2: Detección y corrección de nueva vulnerabilidad
4.1 Escaneo completo del sistema
•Escaneo con nmap, nikto, linpeas, etc.
•Vulnerabilidades encontradas (puertos abiertos, servicios mal configurados)
4.2 Explotación controlada
•Descripción detallada de la explotación (comandos, scripts, vectores)
•Pruebas de escalación (si aplica)
•Evidencia (salida de comandos, logs, capturas)
4.3 Corrección aplicada
•Cambio de configuraciones
•Cierre de puertos
•Validación post-corrección
4.4 Validación de seguridad
•Resultado tras parcheo y nueva revisión
•Checklist antes/después de hardening

5.Fase 3: Plan de respuesta a incidentes y SGSI
5.1 Plan de respuesta a incidentes (NIST SP 800-61)
•Identificación: Cómo detectar futuros incidentes
•Contención: Procedimientos para aislar el sistema
•Erradicación: Eliminación del ataque y su rastro
•Recuperación: Restauración y continuidad operativa
•Lecciones aprendidas: Cómo evitar la recurrencia
5.2 Protección de datos
•Respaldo regular de sistemas
•Cifrado de datos sensibles
•Control de accesos (MFA, roles, auditoría)
5.3 Sistema de Gestión de Seguridad de la Información (SGSI – ISO 27001)
•Análisis de riesgos
•Políticas de seguridad definidas
•Medidas de protección (firewall, acceso, políticas de actualización)
•Planes de mejora continua

6.Conclusiones generales
•Estado inicial vs. estado final del sistema
•Impacto del trabajo realizado
•Lecciones técnicas aprendidas

7.Recomendaciones
•Medidas futuras (2FA, SIEM, backups externos)
•Capacitación al personal
•Escaneos regulares automatizados

8.Glosario
Términos
Definición
Rootkit
Conjunto de herramientas usadas para ocultar procesos maliciosos
NIST
Instituto Nacional de Estándares y Tecnología (EE. UU.)
SGSI
Sistema de Gestión de Seguridad de la Información

9.Referencias
•Guía NIST SP 800-61
•ISO 27001
•Documentación de herramientas: rkhunter, chkrootkit, nmap, etc.

10.Anexos (Algunos anexos no están subidos por capacidad del repositorio o porque están incrustados en el informe)
•Salidas completas de herramientas (nmap, chkrootkit)
•Scripts utilizados (recolectar_evidencia.sh, clonar_disco.sh)
•Capturas de pantalla
•Archivos comprimidos (evidencia.tar.gz, imagen.dd)
