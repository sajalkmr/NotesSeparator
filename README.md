# HandwrittenNotesClassification
A deep learning model to separate Handwritten notes and non notes images with Python and Tensorflow.


<h2>Requirements</h2>
<ul>
	<li>Python 3.6+</li>
	<li>TensorFlow 2.0+</li>
	<li>OpenCV 4.0+</li>
  <li>Numpy</li>
  <li>Json</li>
</ul>

<h2>Usage</h2>
<ol>
	<li>Clone this repository to your local machine.</li>
	<li>Install the required packages listed in the <code>requirements.txt</code> file by running <code>pip install -r requirements.txt</code>.</li>
	<li>Place the images you want to classify in the <code>test_images</code> directory.</li>
	<li>Put your model in the <code>models</code> directory. The model should be saved in the <code>.h5</code> format.</li>
	<li>Run the <code>NotesSeparator.py</code> script to classify the images: <code>NotesSeparator.ipynb </code>if you are running in Jupyter Notebook.</li>
	<li>The classified images will be saved in the <code>output</code> directory.</li>
</ol>

<h2>Example File Structure</h2>
<pre>
	├── classify_notes.py
	├── models
	│   └── notesmodel.h5
	├── output
	│   ├── non_notes
	│   ├── notes
	│   └── results
	│       ├── image1.png
	│       ├── image1.json
	│       ├── image2.png
	│       ├── image2.json
	│       └── results.json
	├── README.md
	└── test_images
	    ├── image1.jpg
	    └── image2.jpg
</pre>

<h2>Model Architecture</h2>
<p>The model used for this project is a Convolutional Neural Network (CNN) with the following layers:</p>
<ol>
	<li>Conv2D layer with 16 filters and a kernel size of (3,3)</li>
	<li>MaxPooling2D layer</li>
	<li>Conv2D layer with 32 filters and a kernel size of (3,3)</li>
	<li>MaxPooling2D layer</li>
	<li>Conv2D layer with 16 filters and a kernel size of (3,3)</li>
	<li>MaxPooling2D layer</li>
	<li>Flatten layer</li>
	<li>Dense layer with 256 neurons</li>
	<li>Dense layer with 1 neuron (output layer) with a sigmoid activation function</li>
</ol>

<h2>Files Saved After Classification</h2>
<p>The classified images are saved in either the <code>notes</code> or <code>non_notes</code> directory in the <code>output</code> folder depending on their classification. Additionally, a <code>results.json</code> file is created in the <code>output/results</code> folder that contains the results of the classification for each image.</p>

<h2>Contributing</h2>
<p>Contributions are welcome. Please fork the repository and submit a pull request.</p>

<h2>License</h2>
<p>This project is licensed under the MIT License.</p>


