<template>
  <div>
    <d-alert class="alert-royal-blue" show>
      <i class="fa fa-info mx-2"></i>
      <strong>How you doin'?</strong> I'm just a friendly, good-looking notification message and I come in all the colors you can see below. Pretty cool, huh?
    </d-alert>

    <d-container fluid class="main-content-container px-4">

      <!-- Page Header -->
      <d-row no-gutters class="page-header py-2 pb-4 mb-3 border-bottom">
        <d-col col sm="4" class="text-center text-sm-left mb-4 mb-sm-0">
          <span class="text-uppercase page-subtitle">Overview</span>
          <h3 class="page-title">Components</h3>
        </d-col>
      </d-row>

      <!-- Colors -->
      <d-row class="mb-2">
        <d-col lg="12">
          <span style="font-size: 16px;" class="d-block mb-2 text-muted"><strong>Colors</strong></span>
        </d-col>
        <d-col class="mb-4">
          <div class="bg-primary rounded text-white text-center p-4" style="box-shadow: inset 0 0 5px rgba(0,0,0,.2);"></div>
        </d-col>
        <d-col class="mb-4">
          <div class="bg-secondary rounded text-white text-center p-4" style="box-shadow: inset 0 0 5px rgba(0,0,0,.2);"></div>
        </d-col>
        <d-col class="mb-4">
          <div class="bg-success rounded text-white text-center p-4" style="box-shadow: inset 0 0 5px rgba(0,0,0,.2);"></div>
        </d-col>
        <d-col class="mb-4">
          <div class="bg-info rounded text-white text-center p-4" style="box-shadow: inset 0 0 5px rgba(0,0,0,.2);"></div>
        </d-col>
        <d-col class="mb-4">
          <div class="bg-warning rounded text-white text-center p-4" style="box-shadow: inset 0 0 5px rgba(0,0,0,.2);"></div>
        </d-col>
        <d-col class="mb-4">
          <div class="bg-danger rounded text-white text-center p-4" style="box-shadow: inset 0 0 5px rgba(0,0,0,.2);"></div>
        </d-col>
        <d-col class="mb-4">
          <div class="bg-dark rounded text-white text-center p-4" style="box-shadow: inset 0 0 5px rgba(0,0,0,.2);"></div>
        </d-col>
      </d-row>

      <d-row>
        <d-col lg="8" class="mb-4">
          <d-card class="card-small mb-4">
            <d-card-header class="border-bottom">
              <h6 class="m-0">Form Inputs</h6>
            </d-card-header>

            <d-list-group flush>
              <d-list-group-item class="p-0 px-3 pt-3">
                <d-row>

                  <!-- Checkboxes -->
                  <d-col sm="12" md="4" class="mb-3">
                    <strong class="text-muted d-block mb-2">Checkboxes</strong>
                    <fieldset>
                      <d-checkbox>Default</d-checkbox>
                      <d-checkbox checked>Checked</d-checkbox>
                      <d-checkbox disabled>Disabled</d-checkbox>
                      <d-checkbox disabled checked>Disabled Checked</d-checkbox>
                    </fieldset>
                  </d-col>

                  <!-- Radio Buttons -->
                  <d-col sm="12" md="4" class="mb-3">
                    <strong class="text-muted d-block mb-2">Radio Buttons</strong>
                    <fieldset>
                      <d-form-radio>Default</d-form-radio>
                      <d-form-radio checked>Checked</d-form-radio>
                      <d-form-radio disabled>Disabled</d-form-radio>
                      <d-form-radio disabled checked>Disabled Checked</d-form-radio>
                    </fieldset>
                  </d-col>

                  <!-- Toggle Buttons -->
                  <d-col sm="12" md="4" class="mb-3">
                    <strong class="text-muted d-block mb-2">Toggle Switches</strong>
                    <fieldset>
                      <d-checkbox toggle class="custom-toggle-sm">Default</d-checkbox>
                      <d-checkbox toggle class="custom-toggle-sm" checked>Checked</d-checkbox>
                      <d-checkbox toggle class="custom-toggle-sm" disabled>Disabled</d-checkbox>
                      <d-checkbox toggle class="custom-toggle-sm" disabled checked>Disabled Checked</d-checkbox>
                    </fieldset>
                  </d-col>

                </d-row>
              </d-list-group-item>

              <d-list-group-item class="p-3">

                <!-- Small Buttons -->
                <strong class="text-muted d-block my-2">Small Buttons</strong>
                <d-row class="mb-3">
                  <d-col>
                    <d-button size="sm" theme="primary" class="mb-2 mr-1">Primary</d-button>
                    <d-button size="sm" theme="secondary" class="mb-2 mr-1">Secondary</d-button>
                    <d-button size="sm" theme="success" class="mb-2 mr-1">Success</d-button>
                    <d-button size="sm" theme="danger" class="mb-2 mr-1">Danger</d-button>
                    <d-button size="sm" theme="warning" class="mb-2 mr-1">Warning</d-button>
                    <d-button size="sm" theme="info" class="mb-2 mr-1">Info</d-button>
                    <d-button size="sm" theme="dark" class="mb-2 mr-1">Dark</d-button>
                    <d-button size="sm" class="mb-2 btn-white mr-1">White</d-button>
                    <d-button size="sm" class="mb-2 btn-royal-blue mr-1">Royal Blue</d-button>
                    <d-button size="sm" class="mb-2 btn-java mr-1">Java</d-button>
                    <d-button size="sm" class="mb-2 btn-salmon mr-1">Salmon</d-button>
                  </d-col>
                </d-row>

                <!-- Small Outline Buttons -->
                <strong class="text-muted d-block my-2">Small Outline Button</strong>
                <d-row>
                  <d-col>
                    <d-button size="sm" outline theme="primary" class="mb-2 mr-1">Primary</d-button>
                    <d-button size="sm" outline theme="secondary" class="mb-2 mr-1">Secondary</d-button>
                    <d-button size="sm" outline theme="success" class="mb-2 mr-1">Success</d-button>
                    <d-button size="sm" outline theme="danger" class="mb-2 mr-1">Danger</d-button>
                    <d-button size="sm" outline theme="warning" class="mb-2 mr-1">Warning</d-button>
                    <d-button size="sm" outline theme="info" class="mb-2 mr-1">Info</d-button>
                    <d-button size="sm" outline theme="dark" class="mb-2 mr-1">Dark</d-button>
                    <d-button size="sm" class="mb-2 btn-outline-light mr-1">Light</d-button>
                    <d-button size="sm" class="mb-2 btn-outline-royal-blue mr-1">Royal Blue</d-button>
                    <d-button size="sm" class="mb-2 btn-outline-java mr-1">Java</d-button>
                    <d-button size="sm" class="mb-2 btn-outline-salmon mr-1">Salmon</d-button>
                  </d-col>
                </d-row>

              </d-list-group-item>

              <d-list-group-item class="p-3">

                <!-- Normal Buttons -->
                <strong class="text-muted d-block my-2">Normal Buttons</strong>
                <d-row>
                  <d-col>
                    <d-button theme="primary" class="mb-2 mr-1">Primary</d-button>
                    <d-button theme="secondary" class="mb-2 mr-1">Secondary</d-button>
                    <d-button theme="success" class="mb-2 mr-1">Success</d-button>
                    <d-button theme="danger" class="mb-2 mr-1">Danger</d-button>
                    <d-button theme="warning" class="mb-2 mr-1">Warning</d-button>
                    <d-button theme="info" class="mb-2 mr-1">Info</d-button>
                    <d-button theme="dark" class="mb-2 mr-1">Dark</d-button>
                    <d-button class="mb-2 btn-white mr-1">White</d-button>
                    <d-button class="mb-2 btn-royal-blue mr-1">Royal Blue</d-button>
                  </d-col>
                </d-row>

                <!-- Normal Outline Buttons -->
                <strong class="text-muted d-block my-2">Normal Outline Buttons</strong>
                <d-row>
                  <d-col>
                    <d-button outline theme="primary" class="mb-2 mr-1">Primary</d-button>
                    <d-button outline theme="secondary" class="mb-2 mr-1">Secondary</d-button>
                    <d-button outline theme="success" class="mb-2 mr-1">Success</d-button>
                    <d-button outline theme="danger" class="mb-2 mr-1">Danger</d-button>
                    <d-button outline theme="warning" class="mb-2 mr-1">Warning</d-button>
                    <d-button outline theme="info" class="mb-2 mr-1">Info</d-button>
                    <d-button outline theme="dark" class="mb-2 mr-1">Dark</d-button>
                    <d-button class="mb-2 btn-outline-light mr-1">Light</d-button>
                    <d-button class="mb-2 btn-outline-royal-blue mr-1">Royal Blue</d-button>
                  </d-col>
                </d-row>

              </d-list-group-item>

              <d-list-group-item class="p-3">
                <d-row>

                  <!-- Forms -->
                  <d-col sm="12" md="6">
                    <strong class="text-muted d-block mb-2">Forms</strong>
                    <d-form>
                      <div class="form-group">
                        <d-input-group prepend="@" class="mb-3">
                          <d-input placeholder="Username" />
                        </d-input-group>
                      </div>
                      <div class="form-group">
                        <d-input type="password" placeholder="Password" value="myCoolPassword" />
                      </div>
                      <div class="form-group">
                        <d-input placeholder="1234 Main St" value="7898 Kensington Junction, New York, USA" />
                      </div>
                      <d-form-row>
                        <d-col md="7">
                          <d-input value="New York" />
                        </d-col>
                        <d-col md="5" class="form-group">
                          <d-select>
                            <option selected>Choose...</option>
                            <option>...</option>
                          </d-select>
                        </d-col>
                      </d-form-row>
                    </d-form>
                  </d-col>

                  <!-- Form Validation -->
                  <d-col sm="12" md="6">
                    <strong class="text-muted d-block mb-2">Form Validation</strong>
                    <d-form validated>
                      <d-form-row>
                        <d-col md="6" class="form-group">
                          <d-input value="Vasile" placeholder="First name" required />
                          <d-form-valid-feedback>The first name looks good!</d-form-valid-feedback>
                        </d-col>

                        <d-col md="6" class="form-group">
                          <d-input value="Catalin" placeholder="Last name" required />
                          <d-form-valid-feedback>The last name looks good!</d-form-valid-feedback>
                        </d-col>
                      </d-form-row>
                      <div class="form-group">
                        <d-input placeholder="Username" required />
                        <d-form-invalid-feedback>The username is taken.</d-form-invalid-feedback>
                      </div>
                      <div class="form-group">
                        <d-select required>
                          <option>Choose</option>
                          <option>...</option>
                        </d-select>
                        <d-form-invalid-feedback>Please select your state</d-form-invalid-feedback>
                      </div>
                    </d-form>
                  </d-col>

                </d-row>
              </d-list-group-item>
            </d-list-group>
          </d-card>

          <d-card class="card-small">

            <!-- Form Example -->
            <d-card-header class="border-bottom">
              <h6 class="m-0">Form Example</h6>
            </d-card-header>

            <d-list-group flush>
              <d-list-group-item class="p-3">
                <d-row>
                  <d-col>
                    <d-form>
                      <d-form-row>
                        <d-col md="6" class="form-group">
                          <label for="feEmailAddress">Email</label>
                          <d-input id="feEmailAddress" type="email" placeholder="Email" />
                        </d-col>
                        <d-col md="6">
                          <label for="fePassword">Password</label>
                          <d-input id="fePassword" type="password" placeholder="Password" />
                        </d-col>
                      </d-form-row>

                      <div class="form-group">
                        <label for="feInputAddress">Address</label>
                        <d-input id="feInputAddress" placeholder="1234 Main St" />
                      </div>

                      <div class="form-group">
                        <label for="feInputAddress2">Address 2</label>
                        <d-input id="feInputAddress2" placeholder="Apartment, Studio, or Floor" />
                      </div>

                      <d-form-row>
                        <d-col md="6" class="form-group">
                          <label for="feInputCity">City</label>
                          <d-input id="feInputCity" />
                        </d-col>
                        <d-col md="4" class="form-group">
                          <label for="feInputState">State</label>
                          <d-select id="feInputState">
                            <option>Choose...</option>
                            <option>...</option>
                          </d-select>
                        </d-col>
                        <d-col md="2" class="form-group">
                          <label for="feInputZip">Zip</label>
                          <d-input id="feInputZip" />
                        </d-col>
                        <d-col md="12" class="form-group">
                          <d-checkbox>I agree with your <a href="#">Privacy Policy</a>.</d-checkbox>
                        </d-col>
                      </d-form-row>
                      <d-button type="submit">Create New Account</d-button>
                    </d-form>
                  </d-col>
                </d-row>
              </d-list-group-item>
            </d-list-group>

          </d-card>
        </d-col>

        <d-col lg="4" class="mb-4">

          <!-- Sliders & Progress Bars -->
          <d-card class="card-small mb-4">
            <d-card-header class="border-bottom">
              <h6 class="m-0">Sliders & Progress Bars</h6>
            </d-card-header>
            <d-list-group flush>
              <d-list-group-item class="px-3">
                <div class="mb-2">
                  <strong class="text-muted d-block mb-3">Progress Bars</strong>

                  <d-progress height="5px" class="mb-3" :value="20" :max="100" />
                  <d-progress theme="royal-blue" height="5px" class="mb-3" :value="40" :max="100" />
                  <d-progress theme="salmon" height="5px" class="mb-3" :value="60" :max="100" />
                  <d-progress theme="warning" height="5px" class="mb-3" :value="80" :max="100" />
                </div>
              </d-list-group-item>
              <d-list-group-item class="px-3">
                <div class="mb-2 pb-1">
                  <strong class="text-muted d-block">Custom Sliders</strong>

                  <d-slider class="slider-success my-4" value="85" :options="{ tooltips: true }" />
                  <d-slider class="slider-royal-blue my-4" value="15" :options="{ connect: [false, true] }" />
                  <d-slider class="my-4 mb-4" :value="35" :options="{ pips: { mode: 'positions', values: [0, 25, 50, 75, 100], density: 5 } }" />
                </div>
              </d-list-group-item>
            </d-list-group>
          </d-card>

          <!-- Groups -->
          <d-card class="card-small mb-4">
            <d-card-header class="border-bottom">
              <h6 class="m-0">Groups</h6>
            </d-card-header>

            <d-list-group flush>
              <d-list-group-item class="px-3">
                <d-form>

                  <!-- Button Groups -->
                  <strong class="text-muted d-block mb-3">Button Groups</strong>

                  <d-button-group class="mb-3">
                    <d-button class="btn-primary">Fizz</d-button>
                    <d-button class="btn-white">Buzz</d-button>
                    <d-button class="btn-white">Foo</d-button>
                    <d-button class="btn-white">Bar</d-button>
                  </d-button-group>

                  <!-- Input Groups -->
                  <strong class="text-muted d-block mb-2">Input Groups</strong>

                  <d-input-group prepend="@" class="mb-3">
                    <d-input placeholder="Username" />
                  </d-input-group>

                  <d-input-group append="@designrevision.com" class="mb-3">
                    <d-input />
                  </d-input-group>

                  <d-input-group prepend="$" append=".00" class="mb-3">
                    <d-input value="1000" />
                  </d-input-group>

                  <!-- Seamless Input Groups -->
                  <strong class="text-muted d-block mb-2">Seamless Input Groups</strong>

                  <d-input-group seamless class="mb-3">
                    <d-input-group-text slot="prepend">
                      <i class="material-icons">person</i>
                    </d-input-group-text>
                    <d-input value="design.revision" />
                  </d-input-group>

                  <d-input-group seamless class="mb-3">
                    <d-input type="password" value="mySuperSecretPassword" />
                    <d-input-group-text slot="append">
                      <i class="material-icons">lock</i>
                    </d-input-group-text>
                  </d-input-group>

                  <d-input-group class="mb-2">
                    <d-input placeholder="Recipient's username" />
                    <d-input-group-addon append>
                      <d-button class="btn-white">Button</d-button>
                    </d-input-group-addon>
                  </d-input-group>

                </d-form>
              </d-list-group-item>
            </d-list-group>
          </d-card>

          <d-card class="card-small">
            <!-- Files & Dropdowns -->
            <d-card-header class="border-bottom">
              <h6 class="m-0">Files & Dropdowns</h6>
            </d-card-header>

            <d-list-group flush>
              <d-list-group-item class="px-3">
                <d-form>

                  <!-- Custom File Upload -->
                  <strong class="text-muted d-block mb-2">Custom File Upload</strong>
                  <div class="custom-file mb-3">
                    <input type="file" class="custom-file-input" id="customFile2" />
                    <label class="custom-file-label" for="customFile2">Choose file...</label>
                  </div>

                  <!-- Dropdown Input Groups -->
                  <strong class="text-muted d-block mb-2">Dropdown Input Groups</strong>
                  <d-input-group class="mb-3">
                    <d-form-input />
                    <d-input-group-addon append>
                      <d-dropdown text="Dropdown" right>
                        <d-dropdown-item>Action A</d-dropdown-item>
                        <d-dropdown-item>Action B</d-dropdown-item>
                      </d-dropdown>
                    </d-input-group-addon>
                  </d-input-group>
                  <d-input-group class="mb-3">
                    <d-input-group-addon prepend>
                      <d-dropdown text="Dropdown" right>
                        <d-dropdown-item>Action A</d-dropdown-item>
                        <d-dropdown-item>Action B</d-dropdown-item>
                      </d-dropdown>
                    </d-input-group-addon>
                    <d-form-input />
                  </d-input-group>

                  <!-- Custom Select -->
                  <strong class="text-muted d-block mb-2">Custom Select</strong>
                  <d-input-group prepend="Options" class="mb-3">
                    <d-select>
                      <option>Choose</option>
                      <option>...</option>
                    </d-select>
                  </d-input-group>
                  <d-input-group append="Options" class="mb-3">
                    <d-select>
                      <option>Choose</option>
                      <option>...</option>
                    </d-select>
                  </d-input-group>

                </d-form>
              </d-list-group-item>
            </d-list-group>
          </d-card>
        </d-col>
      </d-row>
    </d-container>
  </div>
</template>
