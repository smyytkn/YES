import streamlit as st
import pandas as pd

# Başlık
st.title("Merhaba Streamlit 👋")

# Açıklama
st.write("Bu, Streamlit için basit bir örnek uygulamadır.")

# Kullanıcıdan veri alma
isim = st.text_input("Adını gir:")

if isim:
    st.success(f"Hoş geldin, {isim}!")

# Slider örneği
yas = st.slider("Yaşını seç", 0, 100, 22)

st.write(f"Seçilen yaş: {yas}")

# Basit tablo
veri = pd.DataFrame({
    "Ay": ["Ocak", "Şubat", "Mart"],
    "Satış": [120, 150, 180]
})

st.subheader("Örnek Veri Tablosu")
st.dataframe(veri)

# Buton
if st.button("Mesaj Göster"):
    st.balloons()
    st.write("🎉 Streamlit çalışıyor!")
