
add in deploy file->

envFrom:
    - secretRef:
        name: rails-secret

secret ->

code credentials in base64: cat key-base.txt | base64 -w 0

apiVersion: v1
kind: Secret
metadata:
  name: rails-secret
data:
  SECRET_KEY_BASE: xxxxxx
  DATABASE_URL: xxxxx
  GOOGLE_CREDENTIALS: xxxxx

