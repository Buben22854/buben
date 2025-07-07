# buben# Платина — ХТТ: Автозапуск песни на сайте

Этот репозиторий содержит простой HTML-сайт, который автоматически воспроизводит песню **"Платина — ХТТ"** при открытии страницы.

## 🔊 Особенности

- Автоматический запуск аудио при открытии
- Встроенный аудиоплеер
- Совместимость с Vercel, GitHub Pages, Netlify и другими хостингами

## ⚠️ Важно

Современные браузеры могут **блокировать автозапуск звука**. В этом случае:
- Пользователю нужно нажать «Play»
- Или разрешить звук для сайта

## 🚀 Развёртывание на Vercel

1. Распакуйте архив `Platina_Autoplay_Site.zip`
2. Загрузите файлы `index.html` и `platina-htt.mp3` в публичный репозиторий на GitHub
3. Перейдите на [https://vercel.com/import/git](https://vercel.com/import/git)
4. Импортируйте ваш репозиторий
5. Нажмите **Deploy**

Готово! После этого вы получите публичную ссылку на ваш сайт с автозапуском песни.
<audio id="player" controls>
  <source src="platina-htt.mp3" type="audio/mpeg">
  Ваш браузер не поддерживает воспроизведение аудио.
</audio>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    const audio = document.getElementById('player');
    audio.play().catch(() => {
      console.log("Автозапуск заблокирован. Пользователь должен нажать Play.");
    });
  });
</script>
