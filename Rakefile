# == Tasks =====================================================================

# rake new["Title"]
desc 'Create a post in _posts'
task :new, :title do |t, args|
  editor = ENV['EDITOR']

  title = args[:title]
  raise 'Please specify a title.' if title.nil? || title.empty?

  filepath = create_file_with_blog_metadata(title)
  system("#{editor} #{filepath}")
end

# == Helpers ===================================================================

# Generates filename for a given title
def generate_filename(title)
  "#{formatted_current_timestamp}-#{slug_for(title)}.md"
end

# Returns formatted current timestamp
def formatted_current_timestamp
  Time.now.strftime('%Y-%m-%d')
end

# Generates slug for a given title
def slug_for(title)
  dasherized_title = title.downcase.gsub(/\s+/, '-')
  characters_to_remove = /("|'|!|\?|:)/
  dasherized_title.gsub(characters_to_remove, '')
end

# Create a file and populate it with the metadata
def create_file_with_blog_metadata(title)
  filename = generate_filename(title)
  filepath = "_posts/#{filename}"

  raise 'The file already exists.' if File.exists?(filepath)

  blog_metadata = generate_metadata_for(title)
  File.write(filepath, blog_metadata)

  filepath
end

def generate_metadata_for(title)
  "---\nlayout: post\ntitle: #{title}\ndate: '#{formatted_current_timestamp}T12:00:00-05:00'\ntags: []\n---\n"
end
