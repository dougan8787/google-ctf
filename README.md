# google-ctf


<h2>pasteurize</h2>

首先我們打開網站後先看看程式碼，看到了一個留言框，輸入個內容看看，輸入個123，後看看代碼，我們看到
<pre><code>
<!-- TODO: Fix b/1337 in /source that could lead to XSS -->

    <script>
        const note = "123"; /*/
        const note_id = "7706dc51-7508-48e7-8f5b-240fe75a0537";
        const note_el = document.getElementById('note-content');
        const note_url_el = document.getElementById('note-title');
        const clean = DOMPurify.sanitize(note);
        note_el.innerHTML = clean;
        note_url_el.href = `/${note_id}`;
        note_url_el.innerHTML = `${note_id}`;
    </script>
</code></pre>

