# 输出的index.html的模版
> 请考虑方括号里的信息

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>AI News Weekly Updates [这里填入更新日期 <应该是生成所有内容的RSS信息源的更新日期，最近的一个消息源为准>]</title>
    <style>
        body { font-family: sans-serif; display: flex; flex-direction: column; align-items: center; padding: 20px; background-color: #f4f4f9; }
        .audio-container { margin: 20px; border: 1px solid #ddd; padding: 20px; border-radius: 12px; width: 80%; background-color: white; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        h1 { color: #2c3e50; }
        audio { width: 100%; margin-top: 15px; }
        p { white-space: pre-wrap; line-height: 1.6; color: #34495e; font-size: 1.1em; }
        h2 { border-bottom: 2px solid #3498db; padding-bottom: 5px; color: #2980b9; }
        details { margin: 15px 0; }
        summary { cursor: pointer; font-weight: bold; padding: 10px; background-color: #ecf0f1; border-radius: 6px; color: #2c3e50; user-select: none; }
        summary:hover { background-color: #d5dbdb; }
        .transcript { margin-top: 10px; padding: 10px; background-color: #f8f9fa; border-left: 3px solid #3498db; border-radius: 4px; }

        footer { margin-top: 40px; padding: 20px; display: flex; justify-content: center; gap: 30px; border-top: 2px solid #ecf0f1; width: 100%; }
        .icon-btn { display: flex; align-items: center; justify-content: center; width: 50px; height: 50px; border-radius: 50%; background-color: #ecf0f1; cursor: pointer; transition: all 0.3s ease; text-decoration: none; }
        .icon-btn:hover { background-color: #3498db; transform: translateY(-3px); box-shadow: 0 4px 8px rgba(0,0,0,0.2); }
        .icon-btn svg { width: 24px; height: 24px; fill: #2c3e50; transition: fill 0.3s ease; }
        .icon-btn:hover svg { fill: white; }
        .toast { position: fixed; bottom: 30px; right: 30px; background-color: #27ae60; color: white; padding: 15px 25px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.2); opacity: 0; transform: translateY(20px); transition: all 0.3s ease; z-index: 1000; }
        .toast.show { opacity: 1; transform: translateY(0); }

        .modal { display: none; position: fixed; z-index: 2000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.5); }
        .modal.show { display: flex; justify-content: center; align-items: center; }
        .modal-content { background-color: white; padding: 30px; border-radius: 12px; max-width: 600px; width: 90%; box-shadow: 0 8px 16px rgba(0,0,0,0.3); }
        .modal-header { font-size: 1.5em; font-weight: bold; color: #2c3e50; margin-bottom: 20px; }
        .modal-body { background-color: #f8f9fa; padding: 20px; border-radius: 8px; white-space: pre-wrap; line-height: 1.6; color: #34495e; max-height: 400px; overflow-y: auto; margin-bottom: 20px; }
        .modal-footer { display: flex; justify-content: flex-end; gap: 15px; }
        .modal-btn { padding: 12px 24px; border: none; border-radius: 6px; cursor: pointer; font-weight: bold; transition: all 0.3s ease; }
        .modal-btn-primary { background-color: #0077b5; color: white; }
        .modal-btn-primary:hover { background-color: #005885; }
        .modal-btn-secondary { background-color: #ecf0f1; color: #2c3e50; }
        .modal-btn-secondary:hover { background-color: #d5dbdb; }
    </style>
</head>
<body>
    <h1>AI News Weekly Updates - [这里更新日期 <应该是生成所有内容的RSS信息源的更新日期，最近的一个消息源为准>]</h1>
    <div id="content" style="width: 100%; display: flex; flex-direction: column; align-items: center;">

        <div class="audio-container">
            <h2>English</h2>
            <details>
                <summary>📄 Transcript</summary>
                <div class="transcript">
                    <p>[文稿脚本 <英文版本>]</p>
                </div>
            </details>
            <audio controls>
                <source src="[音频文件名字 <英文版本的音频，.mp3扩展名>]" type="audio/mpeg">
            </audio>
        </div>

        [....其他语言的文稿脚本和音频文件，按照以下格式重复....]:
        <div class="audio-container">
            <h2>[语言名称 <如：简体中文、Deutsch等>]</h2>
            <details>
                <summary>📄 [Transcript的翻译 <如：文稿、Transkript等>]</summary>
                <div class="transcript">
                    <p>[文稿脚本 <对应语言的版本>]</p>
                </div>
            </details>
            <audio controls>
                <source src="[音频文件名字 <对应语言的音频，.mp3扩展名>]" type="audio/mpeg">
            </audio>
        </div>

        ......
        ........
        [....其他语言的文稿脚本和音频文件....]
    </div>

    <footer>
        <!-- GitHub Icon -->
        <a href="https://github.com/XinyueZ/TinyAgent/blob/main/tiny_agent/agent/tiny_coding_agent.py" target="_blank" class="icon-btn" title="View on GitHub">
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
            </svg>
        </a>

        <!-- LinkedIn Icon -->
        <a href="#" class="icon-btn" title="Post to LinkedIn" onclick="shareOnLinkedIn(); return false;">
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
            </svg>
        </a>

        <!-- Copy Icon -->
        <a href="#" class="icon-btn" title="Copy link to clipboard" onclick="copyToClipboard(); return false;">
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path d="M16 1H4c-1.1 0-2 .9-2 2v14h2V3h12V1zm3 4H8c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h11c1.1 0 2-.9 2-2V7c0-1.1-.9-2-2-2zm0 16H8V7h11v14z"/>
            </svg>
        </a>
    </footer>

    <div id="toast" class="toast"></div>

    <!-- LinkedIn Post Modal -->
    <div id="linkedinModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">LinkedIn Post Preview</div>
            <div class="modal-body" id="linkedinPostContent"></div>
            <div class="modal-footer">
                <button class="modal-btn modal-btn-secondary" onclick="closeLinkedInModal()">Cancel</button>
                <button class="modal-btn modal-btn-primary" onclick="copyAndOpenLinkedIn()">Copy to Clipboard & Post</button>
            </div>
        </div>
    </div>

    <script>
        const LINKEDIN_POST_TEXT = `🎙️ Stay updated with AI Weekly News! Get the latest AI developments delivered as multilingual audio briefings - perfect for your commute or workout.

✨ Features:
• Weekly AI news summaries
• Available in English, Chinese, and German
• Audio + transcripts for each language
• Clean, accessible interface

• 🧑🏻‍💻 Built with a tiny coding agent: https://github.com/XinyueZ/TinyAgent/blob/main/tiny_agent/agent/tiny_coding_agent.py
• 📗 SKILLS: https://github.com/XinyueZ/-Skills-AI-Weekly-News
• 🔗 Listen now: https://ai-weekly-news.hasszhao.workers.dev/

#AI #MachineLearning #TechNews #Automation`;

        function shareOnLinkedIn() {
            const modal = document.getElementById('linkedinModal');
            const content = document.getElementById('linkedinPostContent');
            content.textContent = LINKEDIN_POST_TEXT;
            modal.classList.add('show');
        }

        function closeLinkedInModal() {
            const modal = document.getElementById('linkedinModal');
            modal.classList.remove('show');
        }

        function copyAndOpenLinkedIn() {
            navigator.clipboard.writeText(LINKEDIN_POST_TEXT).then(() => {
                closeLinkedInModal();
                showToast('✅ Copied! Opening LinkedIn...');
                // Open LinkedIn post creation dialog
                setTimeout(() => {
                    window.open('https://www.linkedin.com/feed/?shareActive=true', '_blank');
                }, 800);
            }).catch(err => {
                showToast('Failed to copy text', true);
            });
        }

        function copyToClipboard() {
            const url = 'https://ai-weekly-news.hasszhao.workers.dev/';
            navigator.clipboard.writeText(url).then(() => {
                showToast('Link copied to clipboard!');
            }).catch(err => {
                showToast('Failed to copy link', true);
            });
        }

        function showToast(message, isError = false) {
            const toast = document.getElementById('toast');
            toast.textContent = message;
            toast.style.backgroundColor = isError ? '#e74c3c' : '#27ae60';
            toast.classList.add('show');
            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }

        // Close modal when clicking outside
        window.onclick = function(event) {
            const modal = document.getElementById('linkedinModal');
            if (event.target === modal) {
                closeLinkedInModal();
            }
        }
    </script>
</body>
</html>
```