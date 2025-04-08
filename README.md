<h2>🧩 Singleton Handler for Unity</h2>

<p>
  This is a generic and flexible <strong>Singleton</strong> implementation designed for 
  <code>MonoBehaviour</code>-based components in Unity. It allows automatic or manual initialization, 
  optional persistence across scenes, and provides an event-based hook upon initialization.
</p>

<h3>💡 Features</h3>
<ul>
  <li>✅ Generic and reusable</li>
  <li>🛠 Optional <code>DontDestroyOnLoad</code> behavior</li>
  <li>⚡ Automatic or manual initialization support</li>
  <li>🔔 <code>OnInitialize</code> event callback when ready</li>
  <li>🧼 Auto-cleanup of duplicate instances</li>
</ul>

<h2>📦 Installation</h2>
    <p>1. Clone this repository:</p>
    <pre><code>git clone https://github.com/berkcankarabulut/SingletonHandler.git</code></pre>
    <p>2. Add it to your Unity project.</p>
    <p>3. Configure the necessary settings.</p>
    
<h3>🧱 Components</h3>

<h3>📦 How to Use</h3>
<ol>
  <li>Inherit from <code>Singleton&lt;YourClass&gt;</code>.</li>
  <li>Access the singleton via <code>YourClass.Instance</code>.</li>
  <li>Override <code>Initialize()</code> and <code>InitializeComplete()</code> if needed.</li>
</ol>

<h3>🧠 Example</h3>

<pre><code>public class AudioManager : Singleton&lt;AudioManager&gt;
{
    protected override void InitializeComplete()
    {
        Debug.Log("AudioManager is ready!");
    }
}
</code></pre>

<h3>📁 Notes</h3>
<ul>
  <li>If <code>autoInitialize</code> is false, you must call <code>Initialize()</code> manually.</li>
  <li>If another instance exists, it will be destroyed automatically to enforce the Singleton pattern.</li>
</ul>
