# milky-prometheus-config
## วิธีการ Deploy

1. Deploy  blackbox-exporter-deployment.yaml 
2. Deploy  bbex-hostlist-for-ping-configmap.yaml
3. Edit Prometheus Operator โดยอ้างอิงจาก prometheus-prometheus.yaml ใส่ส่วนของการนำ Configmap จาก ข้อ 2 Mount ให้อยู่บน Prometheus POD
4. Deploy ScrapeConfig แบบ FileSDConfig ให้ไปเรียกชื่อ host บนไฟล์ targets.yml อยู่ถูก Mount อยู่ใน Prometheus POD ด้วย Step ในข้อที่ 3 
