#מביאה את הIMAGE של פייתון
FROM python:3.11-slim
#עוברת לניתוב-פותחת תיקייה בשם APP ב-container- שאליה יועתקו כל הדברים 
workdir /app

#מעתיקה את קובץ התלויות
COPY requirements.txt .
#מריצה את קובץ התלויות= מתקינה אותם
RUN pip install --no-cache-dir -r requirements.txt
#מעתיקה את קוד השרת ל-CONTAINER
COPY app.py .
#חושף את פורט 8000 - שיהיה פתוח לחוץ - עליו רץ השרת
EXPOSE 8000
#מגדיר שכשהקונטיינר עולה - מיד ירוץ השרת - בשפת PYTHON
CMD ["python","app.py"]
