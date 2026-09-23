---
title: Move to a new device — EigOops
layout: page
---

# Move to a new device — EigOops

<!-- 言語リンク（#english 等）は置かない。URL の # の後ろは引き継ぎの履歴で、
     言語リンクで上書きされると再読み込み後に引き継げなくなる。 -->

<p>
  <a id="open-app" class="open-app" href="#" style="display:inline-block;padding:0.9em 1.6em;border-radius:999px;background:#017999;color:#fff;font-weight:600;text-decoration:none">Open in EigOops</a>
</p>

<p id="no-data" style="display:none">This page is opened from the code shown in EigOops on your old device. Scan that code with this device's camera.</p>

---

## English

You scanned the code shown in EigOops on your old device. Tap **Open in EigOops** above to continue on this device.

- If EigOops is not installed yet, install it from the App Store or Google Play, then scan the code again.
- Your learning history is carried inside the code you scanned. It is not sent to this website.

---

## 日本語

旧端末の EigOops に表示されたコードを読み取りました。上の **Open in EigOops** を押すと、この端末で続きから学べます。

- EigOops をまだ入れていない場合は、App Store または Google Play から入れてから、もう一度コードを読み取ってください。
- 学習の履歴は読み取ったコードの中だけを移動します。このサイトには送られません。

<script>
  (function () {
    var hash = window.location.hash;
    var button = document.getElementById('open-app');
    if (!hash || hash.length < 2) {
      button.style.display = 'none';
      document.getElementById('no-data').style.display = 'block';
      return;
    }
    // 履歴は # の後ろにあり、ブラウザはサーバーへ送らない。同じ中身を
    // 独自スキームでアプリに渡す。
    button.href = 'eigoops://app/eigoops/move' + hash;
  })();
</script>
