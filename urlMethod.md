# BuidUrl
public static URL buildUrl() {
       Uri.Builder builder = new Uri.Builder();
        builder.scheme("https")
               .authority("developer.android.com")
               .appendPath("guide")
               .appendPath("components")
               .appendPath("intents-common")
               .appendQueryParameter(utm_source, udacity)
               .appendQueryParameter(utm_medium, course)
               .appendQueryParameter(utm_campaign, android_basics)
               .fragment("phone")

        URL url = null;
        try {
            url = new URL(builder.toString());
        } catch (MalformedURLException e) {
            e.printStackTrace();
        }
        return url;
    }



