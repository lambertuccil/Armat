# Skill: configurar_red

## Identidad
- **Agente**: IT
- **Nombre**: Configuración de Red
- **Versión**: 1.0

## Objetivo
Configurar y mantener la infraestructura de red de ARMAT, incluyendo internet, WiFi y VPN.

## Entradas
- **tipo_red** (requerido): Internet, WiFi, VPN, LAN
- **dispositivo** (requerido): Router, switch, access point
- **configuracion** (requerido): Parámetros a configurar

## Proceso
1. Identificar necesidad
2. Diseñar configuración
3. Implementar cambios
4. Probar conectividad
5. Documentar configuración
6. Monitorear rendimiento

## Salida
Configuración de red con:
- Parámetros configurados
- Pruebas realizadas
- Documentación actualizada

## Checklist
- [ ] Necesidad identificada
- [ ] Diseño realizado
- [ ] Configuración aplicada
- [ ] Pruebas exitosas
- [ ] Documentado

## Ejemplo
```markdown
# CONFIGURACIÓN WiFi - OFICINA

## Dispositivo: Cisco Meraki MR46
## Ubicación: Sala de juntas

## Configuración
- SSID: ARMAT-Oficina
- Seguridad: WPA3
- VLAN: 10
- Ancho de banda: 200 Mbps

## Pruebas
- Conexión: ✓
- Velocidad: 180 Mbps ✓
- Estabilidad: OK
```
