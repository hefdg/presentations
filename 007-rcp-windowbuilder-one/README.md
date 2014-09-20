<div class="slides">


				<section>
					<h1>Eclipse By Example</h1>
					<h4>Intro to Rich Client Platform and WindowBuilder</h4>
					<p>
						<small>Created by <a href="http://www.skylenewman.com">Kyle Newman</a> with <a href="http://lab.hakim.se/reveal-js/#/">reveal.js</a></small>
					</p>
				</section>
				
				


				<section>
					<h2>Announcements</h2>
					<ul>
						<li class="fragment">GitHub.com/<a href="https://github.com/hefdg" title="HEFDG GitHub" target="_blank">HEFDG</a>
							<ul>
								<li>Roadmap</li>
								<li>Presentations</li>
								<li>Code</li>
							</ul>
						</li>
						<li class="fragment">Website: <a href="http://hsveclipse.com" target="_blank">HSVEclipse.com</a></li>
						<li class="fragment">EclipseCon NA 2015
							<ul>
								<li>March 9 - 12</li>
								<li>Burlingame, CA</li>
								<li><a href="https://www.eclipsecon.org/na2015/about-eclipsecon-na2015" target="_blank">more info</a></li>
							</ul>
						</li>
						<li>Looking for other sponsors (space for 20-40; A/V equipment)</li>
					</ul>
				</section>




				<section>
					<h2>Shameless plugs</h2>
					<h3>Cohesion<em>Force</em> is the bees' knees!</h3>
				</section>




				<section>
					<h2>Ground rules</h2>
					<ul>
						<li class="fragment">Recording for the masses</li>
						<li class="fragment">EPL</li>
						<li class="fragment">Ask questions</li>
						<li class="fragment">Answer questions</li>
						<li class="fragment">Long answer?
							<ul class="fragment">
								<li>Abbreviate first</li>
								<li>Followup after</li>
							</ul>
						</li>
					</ul>
				</section>





				<section>
					<h1>Before we get started, a refresher</h1>
				</section>





				<section>
					<h3>Last month:</h3>
					<ul>
						<li class="fragment">Git</li>
						<li class="fragment">Set up Eclipse</li>
						<li class="fragment">Created models by hand</li>
						<li class="fragment">Generated EXIF model from XML</li>
						<li class="fragment">Generated code
							<ul>
								<li>Model</li>
								<li>Edit</li>
								<li>Editor</li>
								<li>Tests</li>
							</ul>
						</li>
						<li class="fragment">Ran Application</li>
					</ul>
				</section>





				<section>
					<h1>What will we cover today?</h1>
				</section>





				<section>
					<ul>
						<li>Creating a simple RCP Application</li>
						<li class="fragment">Application.e4xmi, part I</li>
						<li class="fragment">Basic View Anatomy</li>
						<li class="fragment">SWT/JFace primer</li>
						<li class="fragment">WindowBuilder, part I</li>
					</ul>
				</section>





				<section>
					But first, set up:
					<ul>
						<li class="fragment">P2 site from http://www.eclipse.org/windowbuilder/download.php</li>
						<li class="fragment">P2 site from http://download.eclipse.org/e4/downloads/
							<ul>
								<li>Eclipse 4 core tools (Incubation)</li>
								<li>Eclipse 4 even spy (Incubation)</li>
								<li>CSS Spy for Eclipse 4(Incubation)</li>
							</ul>
						</li>
						<li class="fragment">Luna update site -> Modeling
							<ul>
								<li>EMF - Eclipse Modeling Framework SDK</li>
								<li>Diagram Editor for Ecore (SDK)</li>
							</ul>
						</li>
					</ul>
				</section>





				<section></section>





				<section>
					<h3>.product file</h3>
					<ul>
						<li>Required Plugins</li>
						<li class="fragment">OSGi Services</li>
						<li class="fragment">Run/Debug as <em><strong>Eclipse</strong></em> application</li>
					
					<li class="fragment"><strong>Tips for RCP Development</strong>
					<ul>
						<li>Run -> Run Configurations -> Clear</li>
						<li>Never 'Add Required Plugins'</li>
					</ul>
				</li>
			</ul>
				</section>





				<section></section>





				<section>
					<h3>.e4xmi</h3>
					<ul>
						<li class="fragment">XML-based</li>
						<li class="fragment">Defines initial application 'workbench' model
							<ul>
								<li class="fragment">Windows</li>
								<li class="fragment">Perspectives</li>
								<li class="fragment">Views</li>
								<li class="fragment">Menus</li>
								<li class="fragment">Keybindings</li>
								<li class="fragment">Other functionality</li>
							</ul>
						</li>
						<li class="fragment">Model can be modified at runtime</li>
					</ul>
				</section>





				<section></section>





				<section>
					<h3>View Anatomy</h3>
					<ul>
						<li class="fragment">Behavior Annotations
							<ul>
								<li class="fragment"><em>@PostConstruct</em></li>
								<li class="fragment"><em>@PreDestroy</em></li>
								<li class="fragment"><em>@Focus</em></li>
								<li class="fragment"><em>@Persist</em></li>
								<li class="fragment"><em>@PersistState</em></li>
							</ul>
						</li>
						<li class="fragment">Injected Objects
							<ul>
								<li class="fragment"><em>@Inject</em> ESelectionService</li>
								<li class="fragment"><em>@Inject</em> public void execute(<em>@Named</em>(IServiceConstants.ACTIVE_...</li>
							</ul>
						</li>
					</ul>
				</section>





				<section>
					<h3>UI Elements in RCP</h3>
					<ul>
						<li class="fragment">SWT
							<ul>
								<li class="fragment">Standard Widget Toolkit</li>
								<li class="fragment">OS* Access to OS**</li>
								<li class="fragment">More native than Swing</li>
								<li class="fragment">AWT bridge</li>
							</ul></li>
						<li class="fragment">JFace
							<ul>
								<li class="fragment">On top of SWT</li>
								<li class="fragment"><em>Viewers</em> simplify mapping of data to visual</li>
								<li class="fragment">Image, color, font support</li>
								<li class="fragment">Data binding support</li>
							</ul></li>
					</ul>
					<small>*Open Source, **Operating System</small>
				</section>





				<section></section>



				


				<section>
					<h1>Thank You!</h1>
					<h4>Need slides? <a href="https://github.com/hefdg/presentations" target="_blank">github.com/hefdg/presentations</a></h4>
					<h4>Want to present? <a href="mailto:kyle@skylenewman.com">kyle@skylenewman.com</a></h4>
				</section>
				


				
			</div>