guard :shell, :all_on_start => true do
  watch /(^.+\.diag$)/ do |m|
    `echo rebuilding "#{m[0]}"...`
    successful = system "seqdiag -Tsvg #{m[0]}"
    if successful
     `echo "...done"`
    else 
      `echo "...failed to build"`
    end
  end
end
   
