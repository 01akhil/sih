
FROM ubuntu:latest

RUN apt-get update && \
    apt-get install -y \
    build-essential \
    python3-pip \
    net-tools \
    iputils-ping \
    iproute2 \
    curl \
    && apt-get clean


RUN curl -fsSL https://deb.nodesource.com/setup_20.x | bash - && \
    apt-get install -y nodejs

RUN npm install -g watchify


WORKDIR /app

COPY package*.json ./


RUN npm install

COPY src/ ./src
COPY src/ /app

COPY src/front-end/html/home.html /app
COPY src/front-end/html/room.html /app
COPY src/front-end/html/sign-in.html /app
COPY src/front-end/html/landing.html /app
COPY src/front-end/html/header.html /app
# COPY src/front-end/html/index.html /app
COPY src/front-end/html/mentee-signup.html /app
COPY src/front-end/html/mentee-login.html /app

COPY src/front-end/html/mentor-signup.html /app
COPY src/front-end/html/mentor-login.html /app

COPY src/front-end/html/mentor-profile.html /app
COPY src/front-end/html/mentee-profile.html /app

COPY src/front-end/html/mentor-dashboard.html /app
COPY src/front-end/html/mentee-dashboard.html /app

COPY src/front-end/html/mentor-details.html /app

COPY src/front-end/css/home_style.css /app
COPY src/front-end/css/room_style.css /app
COPY src/front-end/css/sign-in_style.css /app
COPY src/front-end/css/choice_style.css /app
COPY src/front-end/css/header_style.css /app




COPY src/front-end/client-side-script/bundle.js /app
COPY src/front-end/client-side-script/client.js /app

COPY src/front-end/client-side-script/sign-in.js /app
COPY src/front-end/client-side-script/searchBar.js /app
COPY src/front-end/html/searchBar.html /app
COPY src/front-end/html/paymentButton.html /app
COPY src/front-end/html/paymentFailed.html /app
COPY src/front-end/html/paymentSuccess.html /app

COPY src/front-end/html/mentor-courses.html /app
COPY src/front-end/html/create-course.html /app
COPY src/front-end/html/landing1.html /app
COPY src/front-end/html/upload.html /app
COPY src/front-end/html/page.html /app
COPY src/front-end/html/page2.html /app
COPY src/front-end/html/courses-all.html /app
COPY src/front-end/html/courseDetails.html /app
COPY src/front-end/html/your-courses.html /app
COPY src/front-end/html/mock-interviews.html /app
COPY src/front-end/html/ui.html /app
COPY src/front-end/html/language.html /app
COPY src/front-end/html/photography.html /app
COPY src/front-end/html/mentor-own-courses.html /app
COPY src/front-end/html/mentor-lecture.html /app
COPY src/front-end/html/blog-mentee.html /app


COPY src/front-end/assets/bg.avif /app
COPY src/front-end/assets/mentor.png /app
COPY src/front-end/assets/mentee.png /app
COPY src/front-end/assets/icon.png /app
COPY src/front-end/assets/inbox-alt-1-svgrepo-com.svg /app
COPY src/front-end/assets/exam-a-plus-svgrepo-com.svg /app
COPY src/front-end/assets/dashboard-2-svgrepo-com.svg /app
COPY src/front-end/assets/courses-svgrepo-com.svg /app
COPY src/front-end/assets/blog-website-svgrepo-com.svg /app
COPY src/front-end/assets/logout-svgrepo-com.svg /app



EXPOSE 3000
EXPOSE 2000-2050
EXPOSE 10000-10100

CMD [ "node", "src/server/server.js" ]
