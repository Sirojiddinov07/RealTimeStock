<h1 align="center">Real-Time Stock Application</h1>

<p align="center">
Welcome to the Real-Time Stock application! This project allows users to monitor stock prices in real-time using Django, WebSocket, Celery, and Redis.
</p>

<h2>Features</h2>
<ul>
  <li><strong>Real-Time Stock Updates:</strong> Stay updated with live stock prices through WebSockets.</li>
  <li><strong>Background Tasks:</strong> Celery is used for fetching and processing stock data asynchronously.</li>
  <li><strong>Scalable and Efficient:</strong> Redis is utilized as the message broker and result backend for Celery, ensuring efficient task management.</li>
</ul>

<h2>Technologies Used</h2>
<ul>
  <li><a href="https://www.djangoproject.com/"><strong>Django:</strong></a> The web framework used for building the application.</li>
  <li><a href="https://channels.readthedocs.io/en/stable/"><strong>WebSocket:</strong></a> For real-time communication between the server and clients.</li>
  <li><a href="https://docs.celeryproject.org/en/stable/"><strong>Celery:</strong></a> A task queue for handling asynchronous operations.</li>
  <li><a href="https://redis.io/"><strong>Redis:</strong></a> The in-memory data structure store used as a message broker for Celery.</li>
</ul>

<h2>Installation</h2>
<ol>
  <li><strong>Clone the repository:</strong></li>

<pre>
<code>git clone https://github.com/Sirojiddinov07/RealTimeStock.git
cd RealTimeStock
</code>
</pre>

  <li><strong>Create a virtual environment:</strong></li>

<pre>
<code>python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
</code>
</pre>

  <li><strong>Install the dependencies:</strong></li>

<pre>
<code>pip install -r requirements.txt
</code>
</pre>

  <li><strong>Configure Redis:</strong></li>
  <p>Make sure Redis is installed and running on your machine. You can download it <a href="https://redis.io/download">here</a>.</p>

  <li><strong>Set up the Django project:</strong></li>

<pre>
<code>python manage.py migrate
python manage.py createsuperuser  # Create a superuser for the Django admin
python manage.py runserver
</code>
</pre>

  <li><strong>Run Celery worker:</strong></li>
  <p>In a new terminal window, navigate to your project directory and run:</p>

<pre>
<code>celery -A RealTimeStock worker --loglevel=info
</code>
</pre>

  <li><strong>Access the Application:</strong></li>
  <p>Open your web browser and go to <a href="http://127.0.0.1:8000/">http://127.0.0.1:8000/</a> to start using the Real-Time Stock application.</p>
</ol>

<h2>Usage</h2>
<ul>
  <li><strong>Admin Panel:</strong> You can manage the application via the Django admin panel by accessing <code>/admin/</code>.</li>
  <li><strong>Real-Time Updates:</strong> Stock prices will be updated in real-time on the frontend through WebSockets.</li>
</ul>

<h2>Contributing</h2>
<p>Contributions are welcome! If you'd like to contribute, please fork the repository and submit a pull request.</p>

<h2>License</h2>
<p>This project is licensed under the MIT License. See the <a href="LICENSE">LICENSE</a> file for more details.</p>
