<template>
  <head>
    <meta charset="utf-8">
    <link crossorigin="anonymous" media="all" rel="stylesheet" href="https://github.githubassets.com/assets/light-0946cdc16f15.css" />
    <link crossorigin="anonymous" media="all" rel="stylesheet" href="https://github.githubassets.com/assets/dark-3946c959759a.css" />
    <link crossorigin="anonymous" media="all" rel="stylesheet" href="https://github.githubassets.com/assets/primer-74d10edd4b10.css" />
    <link crossorigin="anonymous" media="all" rel="stylesheet" href="https://github.githubassets.com/assets/global-6124edafbf4c.css" />
    <link crossorigin="anonymous" media="all" rel="stylesheet" href="https://github.githubassets.com/assets/github-06172548f975.css" />
    <title>Sign in to GitHub · GitHub</title>
    <link rel="alternate icon" class="js-site-favicon" type="image/png" href="https://github.githubassets.com/favicons/favicon.png">
  </head>
    <div>
      <div class="position-relative js-header-wrapper">
        <div class="header header-logged-out width-full pt-5 pb-4" role="banner">
          <div class="container clearfix width-full text-center">
            <svg
                height="48"
                aria-hidden="true"
                viewBox="0 0 16 16"
                version="1.1"
                width="48"
                data-view-component="true"
                class="octicon octicon-mark-github"
            >
              <path
                  d="M8 0c4.42 0 8 3.58 8 8a8.013 8.013 0 0 1-5.45 7.59c-.4.08-.55-.17-.55-.38 0-.27.01-1.13.01-2.2 0-.75-.25-1.23-.54-1.48 1.78-.2 3.65-.88 3.65-3.95 0-.88-.31-1.59-.82-2.15.08-.2.36-1.02-.08-2.12 0 0-.67-.22-2.2.82-.64-.18-1.32-.27-2-.27-.68 0-1.36.09-2 .27-1.53-1.03-2.2-.82-2.2-.82-.44 1.1-.16 1.92-.08 2.12-.51.56-.82 1.28-.82 2.15 0 3.06 1.86 3.75 3.64 3.95-.23.2-.44.55-.51 1.07-.46.21-1.61.55-2.33-.66-.15-.24-.6-.83-1.23-.82-.67.01-.27.38.01.53.34.19.73.9.82 1.13.16.45.68 1.31 2.69.94 0 .67.01 1.3.01 1.49 0 .21-.15.45-.55.38A7.995 7.995 0 0 1 0 8c0-4.42 3.58-8 8-8Z"
              ></path>
            </svg>
          </div>
        </div>
      </div>

      <div
          class="application-main"
          data-commit-hovercards-enabled
          data-discussion-hovercards-enabled
          data-issue-and-pr-hovercards-enabled
      >
        <main>
          <div class="auth-form px-3" id="login">
            <div class="auth-form-header p-0">
              <h1>Sign in to GitHub</h1>
            </div>

            <div class="auth-form-body mt-3">
              <form
                  data-turbo="false"
                  action="/session"
                  accept-charset="UTF-8"
                  method="post"
              >
                <label for="login_field">Username or email address</label>
                <input
                    type="text"
                    name="login"
                    id="login_field"
                    class="form-control input-block js-login-field"
                    autocapitalize="off"
                    autocorrect="off"
                    autocomplete="username"
                    autofocus
                />

                <div class="position-relative">
                  <label for="password">Password</label>
                  <input
                      type="password"
                      name="password"
                      id="password"
                      class="form-control form-control input-block js-password-field"
                      autocomplete="current-password"
                  />
                  <input
                      type="submit"
                      name="commit"
                      value="Sign in"
                      class="btn btn-primary btn-block js-sign-in-button"
                      data-disable-with="Signing in…"
                      data-signin-label="Sign in"
                      data-sso-label="Sign in with your identity provider"
                      :development="false"
                  />
                  <a class="label-link position-absolute top-0 right-0" tabindex="0"
                  >Forgot password?</a
                  >
                </div>
              </form>
            </div>

            <p class="login-callout mt-3">
              New to GitHub?
              <a>Create an account</a>.
            </p>
          </div>
        </main>
      </div>

      <div class="footer container-lg p-responsive py-6 mt-6 f6" role="contentinfo">
        <ul class="list-style-none d-flex flex-justify-center">
          <li class="mr-3"><a>Terms</a></li>
          <li class="mr-3"><a>Privacy</a></li>
          <li class="mr-3"><a>Security</a></li>
          <li><a class="Link--secondary">Contact GitHub</a></li>
        </ul>
      </div>
    </div>
  </template>

  <script>
    export default {
      name: 'App',
    };
  </script>

  <style>
    body {
      word-wrap: break-word;
    }

    .auth-form-header h1 {
      margin: 0;
    }

    .auth-form-body label {
      display: block;
      margin-bottom: 0.5rem;
    }

    .auth-form-body input[type='text'],
    .auth-form-body input[type='password'] {
      width: 100%;
      margin-bottom: 1rem;
    }

    .auth-form-body .label-link {
      font-size: 0.875rem;
      margin-top: 0.25rem;
    }

    .login-callout {
      margin-top: 1.5rem;
    }
  </style>
