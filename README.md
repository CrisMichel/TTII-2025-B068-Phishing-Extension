## Sobre el Conjunto de Datos

Los datos provienen de **diversas fuentes públicas y curadas**, todas orientadas a la detección de *phishing* en español.  
Cada archivo mantiene la misma estructura base de **10 columnas**, lo que permitió su combinación posterior en un dataset unificado.

9 columnas originales

| Columna | Descripción |
|----------|--------------|
| `subject` | Asunto del correo. |
| `sender_name` | Nombre del remitente. |
| `sender_email` | Dirección de correo del remitente. |
| `sender_domain` | Dominio del remitente. |
| `body` | Cuerpo del mensaje (texto principal del correo). |
| `url` | URLs detectadas dentro del correo. |
| `cta_text` | Texto asociado al llamado a la acción (si existe). |
| `url_count` | Número de URLs detectadas en el cuerpo. |
| `label` | Clase original del correo (phishing = 1/ legit = 0). |

Durante el procesamiento en Colab se añadio una columna adicional:

| Nueva columna | Descripción |
|----------------|--------------|
| `dataset_name` | Nombre del dataset original del que proviene cada registro. |

---

## 📊 Datasets individuales

Los siguientes archivos fueron empleados antes de la unificación:

| Dataset | Tipo | Registros | Descripción breve |
|----------|------|------------|------------------|
| `Alvarado_phishing_espanol.csv` | Phishing | 42 | Correos en español, algunos con campos incompletos. |
| `Darito_enron_ham.csv` | Legit | 3000 | Correos legítimos del corpus Enron. |
| `Darito_hard_ham.csv` | Legit | 488 | Correos legítimos más difíciles de distinguir de phishing. |
| `Darito_spear_phishing_es.csv` | Phishing | 334 | Ejemplos artificiales de spear-phishing en español. |
| `Darito_traditional_phishing.csv` | Phishing | 3332 | Phishing tradicional con plantillas reales. |
| `Lazaro_dataset_legit.csv` | Legit | 209 | Correos legítimos en español curado manualmente. |
| `Lazaro_dataset_phishing.csv` | Phishing | 211 | Correos phishing en español curado manualmente. |
| `ds_huggingface_legit.csv` | Legit | 586 | Correos phishing en español. |
| `ds_huggingface_phishing.csv` | Phishing | 621 | Correos phishing en español. |
| `Michelin_phishing_email.csv` | Phishing | 12 | Correos transcritos de phishing en español nativos |
| `ds_frida_email.csv` | Phishing | 12 | Correos transcritos de phishing en español nativos |
| `ds_jesse.csv` | Phishing | 12 | Correos transcritos de phishing en español nativos |


**Total combinado:** 8,859 correos  
- **Phishing:** 4,576
- **Legit:** 4,283
→ Distribución balanceada (~51.5% phishing, ~48.5% legit) 1.06 : 1 (checar distribución final)
