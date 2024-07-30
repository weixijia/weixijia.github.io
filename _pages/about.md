<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Xijia Wei Personal Website</title>
    <style>
        /* Custom styles for the news section */
        .news-item:nth-child(n+6) {
            display: none;
        }
        .show-more-button {
            cursor: pointer;
            color: #5dbcd2;
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <h1>Xijia Wei Personal Website</h1>
    <p>Have the courage to follow your heart and intuition. They somehow already know what you truly want to become. Everything else is secondary.</p>
    <p style="text-align: right;">-- Steve Jobs</p>
    <hr color="#FFFFFF" />
    
    <h2>About Me</h2>
    <p>I am currently a PhD student at University College London (UCL) under the supervision of 
    <a href="https://uclic.ucl.ac.uk/people/nadia-berthouze/" style="color:#5dbcd2;">Prof Nadia Berthouze</a>, 
    <a href="https://uclic.ucl.ac.uk/people/youngjun-cho" style="color:#5dbcd2;">Prof Youngjun Cho</a> and 
    <a href="https://www.ucl.ac.uk/jill-dando-institute/about-us/people/academic-staff/kevin-chetty" style="color:#5dbcd2;">Prof Kevin Chetty</a>. 
    I focus on developing machine learning algorithms for novel sensing systems in healthcare. I am investigating multimodal machine learning to allow the model to automatically learn communicative features from multisensory data without human intervention and the need for label-hungary labelled data towards robust performances under various real-life scenarios. I am currently developing a novel RF-fusion sensing system that can recognise and understand human body behaviours across various domains.</p>
    <p>I also serve as a visiting scholar at 
    <a href="https://www.bell-labs.com/about/locations/cambridge-uk/#gref" style="color:#5dbcd2;">Nokia Bell Labs</a> after I did my PhD internship, where I worked on acoustic sensing in healthcare.</p>
    <p>Prior to joining UCL, I studied Artificial Intelligence (MSc) under the supervision of 
    <a href="https://vradu.uk/" style="color:#5dbcd2;">Dr Valentin Radu</a> and Electronics and Electrical Engineering (BEng), supervised by 
    <a href="https://www.eng.ed.ac.uk/about/people/prof-tughrul-arslan/" style="color:#5dbcd2;">Prof Tughrul Arslan</a>, at the University of Edinburgh.</p>
    
    <h2>Research Interests</h2>
    <ul>
        <li>Multimodal Machine Learning</li>
        <li>Self-supervised Learning</li>
        <li>Generative AI</li>
        <li>Ubiquitious Computing</li>
        <li>Multisensory Systems</li>
        <li>Radar Systems</li>
        <li>Wireless Sensing</li>
        <li>Sensor-based Healthcare</li>
        <li>Location Tracking System</li>
    </ul>
    
    <hr color="#FFFFFF" />
    
    <h2>News</h2>
    <ul id="news-list">
        <li class="news-item">[Apr. 2024] I passed my PhD upgrade viva!</li>
        <li class="news-item">[Nov. 2023] I served as an AC reviewer for <a href="https://dl.acm.org/journal/imwut">IMWUT</a>.</li>
        <li class="news-item">[Oct. 2023] I served as an AC reviewer for <a href="https://chi2024.acm.org/">CHI'2024</a>.</li>
        <li class="news-item">[Sept. 2023] Two Papers accepted at ACII 2023 My first-author paper on non-intrusive wireless signal based protective behaviour recognition has been accepted "Leveraging WiFi Sensing toward Automatic Recognition of Protective Behaviors". See you MIT Media Lab, Cambridge, MA, USA. <a href="https://acii-conf.net/2023/">Link</a></li>
        <li class="news-item">[June. 2023] Research Internship at Nokia Bell Labs Cambridge. I started my PhD research internship at the prestigious <a href="https://www.bell-labs.com/about/locations/cambridge-uk/">Bell Labs</a> at Cambridge this summer!</li>
        <!-- Additional news items go here -->
        <li class="news-item">[May. 2023] I served as a PC member for <a href="https://acii-conf.net/">ACII'2023</a>.</li>
        <li class="news-item">[April. 2023] I passed my first-year viva regarding the topic of wireless human sensing!</li>
        <li class="news-item">[Sept. 2022] Invited Talk at HK PolyTechnic University. I give a talk at HK PolyTech, regarding the topic of "Machine-learning based Sensor-fusion Localization". <a href="https://www.polyu.edu.hk/en/aae/news-and-events/event/2022/9/27---research-seminar/">Link</a></li>
        <li class="news-item">[Aug. 2022] Paper accepted at IPIN, 2022. Work with Valentin Radu, "Leveraging Transfer Learning for Robust Multimodal Positioning Systems based on Smartphone Multisensory Data". See you in Beijing, China.</li>
        <li class="news-item">[May. 2022] I joined the UCL Interaction Centre (UCLIC) for my PhD adventure!</li>
        <!-- Add more news items as needed -->
    </ul>
    <p class="show-more-button" onclick="toggleNews()">Show More</p>

    <script>
        function toggleNews() {
            const newsItems = document.querySelectorAll('.news-item:nth-child(n+6)');
            const button = document.querySelector('.show-more-button');
            newsItems.forEach(item => {
                if (item.style.display === 'none') {
                    item.style.display = 'list-item';
                    button.textContent = 'Show Less';
                } else {
                    item.style.display = 'none';
                    button.textContent = 'Show More';
                }
            });
        }
    </script>
</body>
</html>
