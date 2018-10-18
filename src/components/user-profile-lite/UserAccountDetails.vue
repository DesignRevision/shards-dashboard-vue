<template>
  <d-card class="card-small mb-4">

    <!-- Card Header -->
    <d-card-header class="border-bottom">
      <h6 class="m-0">{{ title }}</h6>
    </d-card-header>

    <d-list-group flush>
      <d-list-group-item class="p-3">
        <d-row>
          <d-col>
            <d-form>
              <d-form-row>

                <!-- First Name -->
                <d-col md="6" class="form-group">
                  <label for="feFirstName">First Name</label>
                  <d-form-input type="text" id="feFirstName" placeholder="First Name" value="Sierra" />
                </d-col>

                <!-- Last Name -->
                <d-col md="6" class="form-group">
                  <label for="feLastName">Last Name</label>
                  <d-form-input type="text" id="feLastName" placeholder="Last Name" value="Brooks" />
                </d-col>

              </d-form-row>

              <d-form-row>

                <!-- Email -->
                <d-col md="6" class="form-group">
                  <label for="feEmail">Email</label>
                  <d-form-input type="email" id="feEmail" placeholder="Email Address" value="sierra@example.com" />
                </d-col>

                <!-- Password -->
                <d-col md="6" class="form-group">
                  <label for="fePassword">Password</label>
                  <d-form-input type="password" id="fePassword" placeholder="Last Name" value="EX@MPL#P@$$w0RD" />
                </d-col>

              </d-form-row>

              <!-- Address -->
              <div class="form-group">
                <label for="feInputAddress">Address</label>
                <d-form-input type="text" id="feInputAddress" placeholder="1234 Main St" />
              </div>

              <d-form-row>
                <!-- City -->
                <d-col md="6" class="form-group">
                  <label for="feInputCity">City</label>
                  <d-form-input type="text" id="feInputCity" />
                </d-col>

                <!-- State -->
                <d-col md="4" class="form-group">
                  <label for="feInputState">State</label>
                  <d-select :value="null" id="feInputState">
                    <option :value="null" selected>Choose...</option>
                    <option>...</option>
                  </d-select>
                </d-col>

                <!-- Zip Code -->
                <d-col md="2"  class="form-group">
                  <label for="inputZip">Zip</label>
                  <input type="text" class="form-control" id="inputZip">
                </d-col>

              </d-form-row>

              <d-form-row>

                <!-- Description -->
                <d-col md="12" class="form-group">
                  <label for="feDescription">Description</label>
                  <d-textarea name="feDescription" rows="5"></d-textarea>
                </d-col>
              </d-form-row>

              <d-button type="submit" class="btn-accent">Update Account</d-button>

            </d-form>
          </d-col>
        </d-row>
      </d-list-group-item>
    </d-list-group>
  </d-card>
</template>

<script>
export default {
  name: 'user-account-details',
  props: {
    /**
     * The component title.
     */
    title: {
      type: String,
      default: 'Account Details',
    },
  },
};
</script>
