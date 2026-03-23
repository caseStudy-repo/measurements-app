git checkout -b demo-malicious-demo

#!/bin/bash
echo "Safe demo build"
echo "[DEMO] whoami:"
whoami

if [ -n "$DEMO_SECRET" ]; then
  echo "[DEMO] Secret access confirmed"
  echo "[DEMO] Secret length: ${#DEMO_SECRET}"
  echo "[DEMO] Secret prefix: ${DEMO_SECRET:0:4}****"
else
  echo "[DEMO] Secret not available"
fi


chmod +x demo/build.sh
git add demo/build.sh
git commit -m "Demo poisoned pipeline PR"
git push origin demo-malicious-pr