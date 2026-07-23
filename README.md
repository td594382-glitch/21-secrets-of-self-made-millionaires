<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>21 Secrets | Self-Made Millionaires</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body { height: 100%; overflow: hidden; background: #1a1a2e; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; }
        .app-container { width: 100%; height: 100vh; display: flex; flex-direction: column; position: relative; }
        .slides-wrapper { flex: 1; display: flex; overflow-x: auto; overflow-y: hidden; scroll-snap-type: x mandatory; scroll-behavior: smooth; -webkit-overflow-scrolling: touch; scrollbar-width: none; }
        .slides-wrapper::-webkit-scrollbar { display: none; }
        .slide { min-width: 100vw; height: 100%; scroll-snap-align: start; display: flex; flex-direction: column; position: relative; overflow-y: auto; }
        .slide-header { padding: 40px 28px 24px; color: white; position: relative; flex-shrink: 0; }
        .slide-header::after { content: ''; position: absolute; bottom: -30px; left: 0; right: 0; height: 30px; background: inherit; border-radius: 0 0 50% 50%; }
        .icon-circle { width: 56px; height: 56px; border-radius: 50%; background: rgba(255,255,255,0.2); display: flex; align-items: center; justify-content: center; font-size: 28px; margin-bottom: 14px; backdrop-filter: blur(10px); }
        .secret-label { font-size: 11px; font-weight: 700; opacity: 0.7; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 6px; }
        .secret-title { font-size: 26px; font-weight: 800; line-height: 1.2; margin-bottom: 8px; }
        .secret-sub { font-size: 14px; opacity: 0.85; font-weight: 400; line-height: 1.4; }
        .slide-body { padding: 40px 24px 24px; flex: 1; overflow-y: auto; background: #fafafa; }
        .slide-body p { font-size: 15px; color: #4a5568; line-height: 1.7; margin-bottom: 16px; }
        .slide-body strong { color: #2d3748; }
        .box { padding: 16px 18px; border-radius: 12px; margin-bottom: 14px; font-size: 14px; line-height: 1.6; }
        .box-example { background: #ebf8ff; border-left: 4px solid #4facfe; color: #2b6cb0; }
        .box-quote { background: #fffaf0; border-left: 4px solid #ed8936; color: #744210; font-style: italic; }
        .box-action { background: #f0fff4; border-left: 4px solid #48bb78; color: #276749; font-weight: 600; }
        .dots-container { position: fixed; bottom: 0; left: 0; right: 0; padding: 12px 20px 24px; background: linear-gradient(to top, rgba(255,255,255,0.95), transparent); display: flex; justify-content: center; align-items: center; gap: 8px; z-index: 100; }
        .dot { width: 8px; height: 8px; border-radius: 50%; background: #cbd5e0; transition: all 0.3s ease; cursor: pointer; }
        .dot.active { width: 24px; border-radius: 12px; background: #667eea; }
        .swipe-hint { position: fixed; bottom: 60px; left: 50%; transform: translateX(-50%); background: rgba(0,0,0,0.6); color: white; padding: 8px 16px; border-radius: 20px; font-size: 12px; animation: fadeOut 3s ease 2s forwards; pointer-events: none; z-index: 99; }
        @keyframes fadeOut { to { opacity: 0; visibility: hidden; } }
        .title-slide .slide-header { flex: 1; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; padding-bottom: 60px; }
        .title-slide .slide-header::after { display: none; }
        .title-slide .secret-title { font-size: 42px; margin-bottom: 12px; }
        .title-slide .secret-sub { font-size: 18px; opacity: 0.9; }
        .tags { margin-top: 24px; display: flex; gap: 8px; flex-wrap: wrap; justify-content: center; }
        .tag { padding: 6px 14px; border-radius: 20px; font-size: 12px; font-weight: 600; background: rgba(255,255,255,0.2); backdrop-filter: blur(10px); }
        .end-slide .slide-body { display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; padding: 40px 32px; }
        .end-slide .secret-title { font-size: 32px; }
        .share-btn { margin-top: 30px; padding: 14px 32px; background: #667eea; color: white; border: none; border-radius: 30px; font-size: 16px; font-weight: 700; cursor: pointer; box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4); }
        .g1 { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
        .g2 { background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); }
        .g3 { background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%); }
        .g4 { background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%); }
        .g5 { background: linear-gradient(135deg, #fa709a 0%, #fee140 100%); }
        .g6 { background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); }
        .g7 { background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%); }
        .g8 { background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%); }
        .g9 { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
        .g10 { background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); }
        .g11 { background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%); }
        .g12 { background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%); }
        .g13 { background: linear-gradient(135deg, #fa709a 0%, #fee140 100%); }
        .g14 { background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); }
        .g15 { background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%); }
        .g16 { background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%); }
        .g17 { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
        .g18 { background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); }
        .g19 { background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%); }
        .g20 { background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%); }
        .g21 { background: linear-gradient(135deg, #fa709a 0%, #fee140 100%); }
        .g22 { background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%); }
    </style>
</head>
<body>
    <div class="app-container">
        <div class="slides-wrapper" id="slidesWrapper">
            <div class="slide title-slide">
                <div class="slide-header g1">
                    <div style="font-size: 80px; margin-bottom: 20px;">📖</div>
                    <div class="secret-title">21 Secrets</div>
                    <div class="secret-sub">From Self-Made Millionaires</div>
                    <div style="font-size: 13px; opacity: 0.7; margin-top: 8px;">Notes from a single sitting — distilled for you</div>
                    <div class="tags">
                        <span class="tag">Brian Tracy</span>
                        <span class="tag">Self-Made</span>
                        <span class="tag">Millionaires</span>
                    </div>
                </div>
                <div class="slide-body">
                    <p style="text-align: center; font-size: 16px;">Swipe to explore each secret with real-world examples and action steps you can use today. 👉</p>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g1">
                    <div class="icon-circle">🎯</div>
                    <div class="secret-label">Secret 1</div>
                    <div class="secret-title">Dream Big Dreams</div>
                    <div class="secret-sub">Practice "Back From The Future" Thinking</div>
                </div>
                <div class="slide-body">
                    <p>Don't just wish — <strong>project yourself forward 5 years</strong> and look back. What does your ideal life look like? Be specific.</p>
                    <div class="box box-example">💡 <strong>Example:</strong> Instead of "I want to be rich," ask: "What am I doing at 9 AM on a Tuesday? Where do I work? How much is in my bank account? What's my lifestyle?" Write it down like a movie scene.</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> Close your eyes. It's 2031. You're living your best life. Describe 5 things you see, hear, and feel. That's your target.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g2">
                    <div class="icon-circle">🧭</div>
                    <div class="secret-label">Secret 2</div>
                    <div class="secret-title">Develop a Clear Sense of Direction</div>
                    <div class="secret-sub">The 6-Step Goal-Setting Formula</div>
                </div>
                <div class="slide-body">
                    <p>Vague wishes become real goals when you follow this system:</p>
                    <p>1. Decide exactly what you want in each area<br>2. Write them down clearly<br>3. Set a deadline — give yourself a target<br>4. List the activities/effort needed<br>5. Organize into a daily plan<br>6. Take action immediately</p>
                    <div class="box box-example">💡 <strong>Example:</strong> "I want to get fit" → "I will lose 10kg by December 31st by going to the gym 4x/week, meal prepping Sundays, and tracking calories daily."</div>
                    <div class="box box-quote">Write goals as if 1 year has passed and you've already achieved them. Begin each with "I..."</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> Pick ONE goal. Run it through all 6 steps right now.</div>
                    <p style="font-size: 13px; color: #a0aec0;">⚡ Only 3% of adults do this. That 3% outperforms the other 97% combined.</p>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g3">
                    <div class="icon-circle">👤</div>
                    <div class="secret-label">Secret 3</div>
                    <div class="secret-title">See Yourself as Self-Employed</div>
                    <div class="secret-sub">Accept Complete Responsibility</div>
                </div>
                <div class="slide-body">
                    <p>Even if you have a boss, <strong>YOU are the CEO of your life</strong>. No one is coming to save you. The moment you own everything, you gain control of everything.</p>
                    <div class="box box-example">💡 <strong>Example:</strong> Two people work the same job. One says "They don't pay me enough to care." The other says "How can I add so much value they have to pay me more?" Guess who gets promoted?</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> Repeat after yourself: "I am self-employed." Say it until you believe it. Your career is your business.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g4">
                    <div class="icon-circle">❤️</div>
                    <div class="secret-label">Secret 4</div>
                    <div class="secret-title">Do What You Love to Do</div>
                    <div class="secret-sub">Identify What Lights You Up — That's Your Leverage</div>
                </div>
                <div class="slide-body">
                    <p>You can't out-hustle someone who loves what they do. Passion is fuel. When work feels like play, you'll work longer, harder, and better than anyone else.</p>
                    <div class="box box-example">💡 <strong>Example:</strong> A gamer who loves strategy games starts a YouTube channel analyzing game mechanics. They'd play anyway — now they get paid for it. That's leverage.</div>
                    <div class="box box-quote">"The only way to do great work is to love what you do." — Steve Jobs</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> What would you do for free? That's your starting point. Now find a way to monetize it.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g5">
                    <div class="icon-circle">⭐</div>
                    <div class="secret-label">Secret 5</div>
                    <div class="secret-title">Commit to Excellence</div>
                    <div class="secret-sub">Decide to Be the Best</div>
                </div>
                <div class="slide-body">
                    <p>At the beginning, you'll suck. But because of your commitment to excellence, <strong>you'll grow more</strong>. Excellence is a decision, not a starting point.</p>
                    <div class="box box-example">💡 <strong>Example:</strong> Your first podcast episode will be terrible. Your 50th will be decent. Your 200th will be world-class. The only difference? You kept going.</div>
                    <div class="box box-quote"><strong>Power Question:</strong> "What one skill, if I developed and did it in an excellent fashion, would have the greatest positive impact on my life?" (For the author: Storytelling and Speaking)</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> Pick ONE skill. Master it. Excellence in one thing beats mediocrity in ten.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g6">
                    <div class="icon-circle">⚡</div>
                    <div class="secret-label">Secret 6</div>
                    <div class="secret-title">Work Longer and Harder</div>
                    <div class="secret-sub">Work All the Time You Work</div>
                </div>
                <div class="slide-body">
                    <p>The average person works about 3 real hours in an 8-hour day. The rest is scrolling, chatting, and "looking busy." <strong>When you work, work.</strong></p>
                    <div class="box box-example">💡 <strong>Example:</strong> Two freelancers both "work" 8 hours. One actually produces for 2 hours. The other produces for 7. In one year, the second person has done 3.5x more work. That's the gap between average and extraordinary.</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> Track your actual productive hours today. Be honest. Then add just ONE more focused hour tomorrow.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g7">
                    <div class="icon-circle">📚</div>
                    <div class="secret-label">Secret 7</div>
                    <div class="secret-title">Dedicate Yourself to Lifelong Learning</div>
                    <div class="secret-sub">Train Your Mind Daily</div>
                </div>
                <div class="slide-body">
                    <p>The world rewards the learned. If you're not growing, you're dying. <strong>Make learning non-negotiable.</strong></p>
                    <div class="box box-example">💡 <strong>Example:</strong> A salesperson who reads one sales book per month knows 12x more closing techniques than a colleague who doesn't. In 3 years, the gap is unbridgeable.</div>
                    <div class="box box-quote">"In 5 years, you'll be the same person you are today except for the books you read and the people you meet."</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> What's ONE book in your field you haven't read? Start it tonight. 20 pages.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g8">
                    <div class="icon-circle">💰</div>
                    <div class="secret-label">Secret 8</div>
                    <div class="secret-title">Pay Yourself First</div>
                    <div class="secret-sub">Save 10% of Your Income</div>
                </div>
                <div class="slide-body">
                    <p>Before bills, before fun, before anything — <strong>pay your future self</strong>. This one habit separates the wealthy from the broke.</p>
                    <div class="box box-example">💡 <strong>Example:</strong> You earn $2,000/month. Pay yourself $200 first. In 10 years at 7% return, that's $34,000. In 30 years? $245,000. From just $200/month. The math doesn't lie.</div>
                    <div class="box box-quote"><strong>The 30-Day Rule:</strong> The longer you delay a purchase, the better you get at deciding if it's worth your money.</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> Set up an auto-transfer of 10% on payday. You won't miss it. Your future self will thank you.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g9">
                    <div class="icon-circle">🔍</div>
                    <div class="secret-label">Secret 9</div>
                    <div class="secret-title">Learn Every Detail of Your Business</div>
                    <div class="secret-sub">The Market Pays for Excellent Performance</div>
                </div>
                <div class="slide-body">
                    <p>The Law of Integrative Complexity: <strong>The person who can integrate and use the greatest amount of information in any field soon rises to the top.</strong></p>
                    <div class="box box-example">💡 <strong>Example:</strong> A barista who knows coffee origins, brewing science, and customer psychology becomes a coffee shop owner. The one who just presses buttons stays a barista.</div>
                    <div class="box box-action">🎬 <strong>Exercise:</strong> Identify trends in your business. What core competencies will you need to lead your field in the future? Make a plan to develop those skills — and work on them every day.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g10">
                    <div class="icon-circle">🤝</div>
                    <div class="secret-label">Secret 10</div>
                    <div class="secret-title">Dedicate Yourself to Serving Others</div>
                    <div class="secret-sub">Help Others Get What They Want</div>
                </div>
                <div class="slide-body">
                    <p>Zig Ziglar's law: <strong>"You can get everything you want in life if you just help enough other people get what they want."</strong></p>
                    <div class="box box-example">💡 <strong>Example:</strong> A real estate agent who obsesses over finding the PERFECT home for clients (not just closing deals) gets referrals for life. One happy client brings 3 more. One unhappy client costs you 10.</div>
                    <div class="box box-quote"><strong>Do More Than Required.</strong> If you do what IS required, you will get what IS required. Do more, friend.</div>
                    <div class="box box-action">🎬 <strong>Your Turn:</strong> Go above and beyond on ONE thing today. Not for recognition — because that's who you are.</div>
                </div>
            </div>
            <div class="slide">
                <div class="slide-header g11">
                    <div class="icon-circle">🤲</div>
                    <div class="secret-label">Secret 11</div>
                    <div class="secret-title">Be Honest With Yourself and Others</div>
                    <div class="secret-sub">Your Word Is Your Bond</div>
                </div>
                <div class="slide-body">
                    <p>Integrity compounds. Every promise kept builds trust. Every promise broken destroys it. <strong>Trust is the currency of relationships.</strong></p>
                    <div class="box box-example">💡 <strong>Example:</strong> You tell a client "I'll send it by Friday." It's Thursday night and you're tired. You send it anyway. That one action builds a reputation 
