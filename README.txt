GESTIÓN DE AUTORIZACIONES – DOA CORTEVA
========================================

CONFIGURACIÓN OFICIAL DE ESTA PLATAFORMA
----------------------------------------
Proyecto Supabase utilizado exclusivamente por esta plataforma:
https://xpcwcqhfuepnykhukjrc.supabase.co

Clave Publishable utilizada por index.html:
sb_publishable_v6jXdDSkzB_jd7K10Oo0Kg_KSATAgqA

La plataforma consulta y guarda sus datos mediante la configuración de Supabase incluida en index.html.
Los archivos SQL se ejecutan manualmente en el SQL Editor del proyecto indicado; subirlos a GitHub no los ejecuta.

PUBLICACIÓN
----------
Archivo principal: index.html
Repositorio: Doa-Mantenimiento

ARCHIVOS SQL
-----------
- SUPABASE_ADMIN_POLICIES.sql: políticas administrativas para perfiles, estándares/DOA y usuarios.
- SUPABASE_HISTORIAL_CAMBIOS.sql: tabla de auditoría y triggers para registrar INSERT, UPDATE y DELETE.
- SUPABASE_PUBLIC_VIEW_POLICIES.sql: políticas de lectura y permisos de escritura para cumplimiento.

IMPORTANTE SOBRE SEGURIDAD
--------------------------
La clave Publishable está diseñada para usarse en el navegador. Nunca publiques claves Secret/service_role ni contraseñas.

SUPABASE_PUBLIC_VIEW_POLICIES.sql habilita lectura pública de usuarios y cumplimiento. Esto puede exponer datos de empleados y registros de cumplimiento. Revisa las políticas y los permisos antes de ejecutarlas y confirma que coincidan con la privacidad requerida.

El script de historial depende de public.is_doa_admin(), definida en SUPABASE_ADMIN_POLICIES.sql. Si instalas el historial por separado, ejecuta primero las políticas administrativas.

Los archivos SQL deben ejecutarse únicamente en el proyecto Supabase indicado al inicio. Después, prueba que la plataforma pueda consultar, registrar y actualizar información correctamente.
