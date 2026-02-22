# 📊Sales Forecasting System

تطبيق مبني باستخدام Streamlit يتيح توقع المبيعات بناءً على مدخلات المستخدم.

## وصف سريع
يقوم النظام بتوقع المبيعات بناءً على:
- تاريخ الطلب (Order Date)
- القطاع (Segment)
- وجود عرض ترويجي (Promotion Flag)
- معرف المنتج (Product ID)
- الدولة (Country)

ويتم تحويل هذه المدخلات داخليًا إلى الخصائص التي تدرب عليها النموذج، ثم يتم تنفيذ التوقع.

---

##  ملفات المشروع:
- `app.py` : الواجهة التفاعلية عبر Streamlit.
- `model.pkl` : النموذج المدرب على بيانات المبيعات.
- `encoders.pkl` : يحتوي على LabelEncoders لـ Country وProduct.
- `onehot_encoders.pkl` : يحتوي على OneHotEncoders لـ Season وSegment وCategory.
- `training_columns.txt` : الأعمدة المستخدمة أثناء التدريب (لضمان التطابق وقت التنبؤ).

---

##  طريقة التشغيل محليًا:

```bash
pip install -r requirements.txt
streamlit run app.py
```

---

##  النشر على الإنترنت:
- يمكنك رفع المشروع على [Streamlit Cloud](https://streamlit.io/cloud) مجانًا.

---

##  ملاحظات:
- يجب أن تكون جميع القيم المدخلة (مثل Segment أو Country) ضمن القيم التي تم تدريب النموذج عليها.
- في حال ظهور خطأ، تحقق من أن أسماء الأعمدة متوافقة مع `training_columns.txt`.

---

تم تطوير هذا المشروع كجزء من مشروع تحليل البيانات وتعلم الآلة.

